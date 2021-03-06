---
title: Procedimiento Recorrer en iteración todos los nodos de un Control TreeView de formularios Windows Forms
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- TreeView control [Windows Forms], iterating through nodes
- tree nodes in TreeView control [Windows Forms], iterating through
ms.assetid: 427f8928-ebcf-4beb-887f-695b905d5134
ms.openlocfilehash: c6345ab5e5d4f4e480bb2724e7a1d795de2bef5d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54651856"
---
# <a name="how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control"></a>Procedimiento Recorrer en iteración todos los nodos de un Control TreeView de formularios Windows Forms
A veces es útil examinar todos los nodos en un formulario Windows Forms <xref:System.Windows.Forms.TreeView> control con el fin de realizar algún cálculo en los valores de nodo. Esta operación puede realizarse mediante un procedimiento recursivo (un método recursivo en C# y C++) que recorre en iteración los nodos de cada colección del árbol.  
  
 Cada <xref:System.Windows.Forms.TreeNode> objeto en una vista de árbol tiene propiedades que puede usar para navegar por la vista de árbol: <xref:System.Windows.Forms.TreeNode.FirstNode%2A>, <xref:System.Windows.Forms.TreeNode.LastNode%2A>, <xref:System.Windows.Forms.TreeNode.NextNode%2A>, <xref:System.Windows.Forms.TreeNode.PrevNode%2A>, y <xref:System.Windows.Forms.TreeNode.Parent%2A>. El valor de la <xref:System.Windows.Forms.TreeNode.Parent%2A> propiedad es el nodo primario del nodo actual. Los nodos secundarios del nodo actual, si existe alguna, se muestran en su <xref:System.Windows.Forms.TreeNode.Nodes%2A> propiedad. El <xref:System.Windows.Forms.TreeView> propio control tiene el <xref:System.Windows.Forms.TreeView.TopNode%2A> propiedad, que es el nodo raíz de la vista de árbol completa.  
  
### <a name="to-iterate-through-all-nodes-of-the-treeview-control"></a>Para recorrer en iteración todos los nodos del control TreeView  
  
1.  Cree un procedimiento recursivo (un método recursivo en C# y C++) que compruebe cada nodo.  
  
2.  Llame al procedimiento.  
  
     El ejemplo siguiente muestra cómo imprimir cada <xref:System.Windows.Forms.TreeNode> del objeto <xref:System.Windows.Forms.TreeNode.Text%2A> propiedad:  
  
    ```vb  
    Private Sub PrintRecursive(ByVal n As TreeNode)  
       System.Diagnostics.Debug.WriteLine(n.Text)  
       MessageBox.Show(n.Text)  
       Dim aNode As TreeNode  
       For Each aNode In n.Nodes  
          PrintRecursive(aNode)  
       Next  
    End Sub  
  
    ' Call the procedure using the top nodes of the treeview.  
    Private Sub CallRecursive(ByVal aTreeView As TreeView)  
       Dim n As TreeNode  
       For Each n In aTreeView.Nodes  
          PrintRecursive(n)  
       Next  
    End Sub  
    ```  
  
    ```csharp  
    private void PrintRecursive(TreeNode treeNode)  
    {  
       // Print the node.  
       System.Diagnostics.Debug.WriteLine(treeNode.Text);  
       MessageBox.Show(treeNode.Text);  
       // Print each node recursively.  
       foreach (TreeNode tn in treeNode.Nodes)  
       {  
          PrintRecursive(tn);  
       }  
    }  
  
    // Call the procedure using the TreeView.  
    private void CallRecursive(TreeView treeView)  
    {  
       // Print each node recursively.  
       TreeNodeCollection nodes = treeView.Nodes;  
       foreach (TreeNode n in nodes)  
       {  
          PrintRecursive(n);  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void PrintRecursive( TreeNode^ treeNode )  
       {  
          // Print the node.  
          System::Diagnostics::Debug::WriteLine( treeNode->Text );  
          MessageBox::Show( treeNode->Text );  
  
          // Print each node recursively.  
          System::Collections::IEnumerator^ myNodes = (safe_cast<System::Collections::IEnumerable^>(treeNode->Nodes))->GetEnumerator();  
          try  
          {  
             while ( myNodes->MoveNext() )  
             {  
                TreeNode^ tn = safe_cast<TreeNode^>(myNodes->Current);  
                PrintRecursive( tn );  
             }  
          }  
          finally  
          {  
             IDisposable^ disposable = dynamic_cast<System::IDisposable^>(myNodes);  
             if ( disposable != nullptr )  
                      disposable->Dispose();  
          }  
       }  
  
       // Call the procedure using the TreeView.  
       void CallRecursive( TreeView^ treeView )  
       {  
          // Print each node recursively.  
          TreeNodeCollection^ nodes = treeView->Nodes;  
          System::Collections::IEnumerator^ myNodes = (safe_cast<System::Collections::IEnumerable^>(nodes))->GetEnumerator();  
          try  
          {  
             while ( myNodes->MoveNext() )  
             {  
                TreeNode^ n = safe_cast<TreeNode^>(myNodes->Current);  
                PrintRecursive( n );  
             }  
          }  
          finally  
          {  
             IDisposable^ disposable = dynamic_cast<System::IDisposable^>(myNodes);  
             if ( disposable != nullptr )  
                      disposable->Dispose();  
          }  
       }  
    ```  
  
## <a name="see-also"></a>Vea también
- [TreeView (control)](../../../../docs/framework/winforms/controls/treeview-control-windows-forms.md)
- [Procedimientos recursivos](~/docs/visual-basic/programming-guide/language-features/procedures/recursive-procedures.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 42fb10ef388fdda9616f78453163db822da9d036
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935289"
---
# <span data-ttu-id="71e28-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="71e28-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="71e28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e28-102">SYNOPSIS</span></span>
<span data-ttu-id="71e28-103">Eltávolít egy SQL Server-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="71e28-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="71e28-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71e28-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e28-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71e28-105">DESCRIPTION</span></span>
<span data-ttu-id="71e28-106">A **Remove-AzVMSqlServerExtension** parancsmag eltávolítja az AzureSQL Server-bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="71e28-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="71e28-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71e28-107">EXAMPLES</span></span>

### <span data-ttu-id="71e28-108">1. példa: SQL Server-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="71e28-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="71e28-109">Ez a parancs eltávolít egy SQL Server-bővítményt a ContosoVM22 nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="71e28-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="71e28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71e28-110">PARAMETERS</span></span>

### <span data-ttu-id="71e28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e28-111">-DefaultProfile</span></span>
<span data-ttu-id="71e28-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71e28-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e28-113">-Name</span><span class="sxs-lookup"><span data-stu-id="71e28-113">-Name</span></span>
<span data-ttu-id="71e28-114">Annak az SQL Servernek a nevét adja meg, amelyről a parancsmag eltávolítja a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="71e28-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e28-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71e28-115">-NoWait</span></span>
<span data-ttu-id="71e28-116">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="71e28-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="71e28-117">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="71e28-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e28-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e28-118">-ResourceGroupName</span></span>
<span data-ttu-id="71e28-119">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="71e28-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e28-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="71e28-120">-VMName</span></span>
<span data-ttu-id="71e28-121">Annak a virtuális gépnek a nevét adja meg, amelyből a parancsmag eltávolítja az SQL Server-bővítményt.</span><span class="sxs-lookup"><span data-stu-id="71e28-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e28-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e28-122">CommonParameters</span></span>
<span data-ttu-id="71e28-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e28-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e28-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71e28-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e28-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71e28-125">INPUTS</span></span>

### <span data-ttu-id="71e28-126">System.String</span><span class="sxs-lookup"><span data-stu-id="71e28-126">System.String</span></span>

## <span data-ttu-id="71e28-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e28-127">OUTPUTS</span></span>

### <span data-ttu-id="71e28-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="71e28-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="71e28-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71e28-129">NOTES</span></span>

## <span data-ttu-id="71e28-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71e28-130">RELATED LINKS</span></span>

[<span data-ttu-id="71e28-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="71e28-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="71e28-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="71e28-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



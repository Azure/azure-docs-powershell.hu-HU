---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478433"
---
# <span data-ttu-id="0d797-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0d797-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="0d797-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d797-102">SYNOPSIS</span></span>
<span data-ttu-id="0d797-103">Eltávolít egy DSC-csomópontot egy automatizálási fiók kezelésével.</span><span class="sxs-lookup"><span data-stu-id="0d797-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="0d797-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0d797-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d797-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0d797-105">DESCRIPTION</span></span>
<span data-ttu-id="0d797-106">A **Unregister-AzAutomationDscNode** parancsmag eltávolítja az APS kívánt államkonfigurációs (DSC) csomópontját az Azure Automation-fiók kezeléséből.</span><span class="sxs-lookup"><span data-stu-id="0d797-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="0d797-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0d797-107">EXAMPLES</span></span>

### <span data-ttu-id="0d797-108">1. példa: Azure DSC-csomópont eltávolítása automatizálási fiók kezelésből</span><span class="sxs-lookup"><span data-stu-id="0d797-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="0d797-109">Ez a parancs eltávolítja azt a DSC-csomópontot, amely a megadott GUID azonosítóval rendelkezik a Contoso17 nevű automatizálási fiók kezelésében.</span><span class="sxs-lookup"><span data-stu-id="0d797-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0d797-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d797-110">PARAMETERS</span></span>

### <span data-ttu-id="0d797-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0d797-111">-AutomationAccountName</span></span>
<span data-ttu-id="0d797-112">Annak az automatizálási fióknak a nevét adja meg, amelyből a parancsmag eltávolít egy DSC-csomópontot.</span><span class="sxs-lookup"><span data-stu-id="0d797-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d797-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d797-113">-DefaultProfile</span></span>
<span data-ttu-id="0d797-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0d797-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d797-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0d797-115">-Force</span></span>
<span data-ttu-id="0d797-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0d797-116">ps_force</span></span>

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

### <span data-ttu-id="0d797-117">-Id</span><span class="sxs-lookup"><span data-stu-id="0d797-117">-Id</span></span>
<span data-ttu-id="0d797-118">A parancsmag által eltávolított DSC-csomópont egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0d797-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d797-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d797-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d797-120">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag nem regisztrál egy DSC-csomópontot.</span><span class="sxs-lookup"><span data-stu-id="0d797-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="0d797-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d797-121">-Confirm</span></span>
<span data-ttu-id="0d797-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0d797-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d797-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d797-123">-WhatIf</span></span>
<span data-ttu-id="0d797-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0d797-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d797-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0d797-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d797-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d797-126">CommonParameters</span></span>
<span data-ttu-id="0d797-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d797-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d797-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d797-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d797-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d797-129">INPUTS</span></span>

### <span data-ttu-id="0d797-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0d797-130">System.Guid</span></span>

### <span data-ttu-id="0d797-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0d797-131">System.String</span></span>

## <span data-ttu-id="0d797-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d797-132">OUTPUTS</span></span>

### <span data-ttu-id="0d797-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="0d797-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="0d797-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0d797-134">NOTES</span></span>

## <span data-ttu-id="0d797-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d797-135">RELATED LINKS</span></span>

[<span data-ttu-id="0d797-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0d797-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="0d797-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0d797-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="0d797-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0d797-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)



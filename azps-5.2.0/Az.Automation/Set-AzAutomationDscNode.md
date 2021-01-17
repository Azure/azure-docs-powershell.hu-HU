---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 02a6d7a129dc084b982f1827d678354265ddbc66
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373097"
---
# <span data-ttu-id="0045f-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0045f-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="0045f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0045f-102">SYNOPSIS</span></span>
<span data-ttu-id="0045f-103">Módosítja azt a csomópontkonfigurációt, amelyhez a DSC-csomópont megfeleltetve van.</span><span class="sxs-lookup"><span data-stu-id="0045f-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="0045f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0045f-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0045f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0045f-105">DESCRIPTION</span></span>
<span data-ttu-id="0045f-106">A **Set-AzAutomationDscNode** parancsmag módosítja az APS kívánt állapotkonfigurációs (DSC) csomópont-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0045f-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="0045f-107">Az Azure Automation felügyelt objektumformátumú (MOF) konfigurációs dokumentumként tárolja a DSC-csomópontok konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0045f-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="0045f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0045f-108">EXAMPLES</span></span>

### <span data-ttu-id="0045f-109">1. példa: Csomópontkonfigurációs megfeleltetés módosítása</span><span class="sxs-lookup"><span data-stu-id="0045f-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="0045f-110">Ez a parancs hozzárendeli a Contoso.NodeConfiguration01 nevű csomópont-konfigurációt ahhoz a csomóponthoz, amely rendelkezik a megadott GUID azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="0045f-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="0045f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0045f-111">PARAMETERS</span></span>

### <span data-ttu-id="0045f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0045f-112">-AutomationAccountName</span></span>
<span data-ttu-id="0045f-113">Annak az automatizálási fióknak a nevét adja meg, amely azt a DSC-csomópontot tartalmazza, amelynek a parancsmagja módosítja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0045f-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="0045f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0045f-114">-DefaultProfile</span></span>
<span data-ttu-id="0045f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0045f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0045f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0045f-116">-Force</span></span>
<span data-ttu-id="0045f-117">ps_force parancs futtatásához nem kell felhasználói megerősítést kérnie.</span><span class="sxs-lookup"><span data-stu-id="0045f-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0045f-118">-Id</span><span class="sxs-lookup"><span data-stu-id="0045f-118">-Id</span></span>
<span data-ttu-id="0045f-119">Annak a DSC-csomópontnak az egyedi azonosítója, amelynek a parancsmagja módosítja a konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0045f-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="0045f-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0045f-120">-NodeConfigurationName</span></span>
<span data-ttu-id="0045f-121">Annak a csomópont-konfigurációnak a nevét adja meg, amelyhez ez a parancsmag leképezi a csomópontot.</span><span class="sxs-lookup"><span data-stu-id="0045f-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0045f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0045f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0045f-123">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag módosítja a DSC-csomópont konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0045f-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="0045f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0045f-124">-Confirm</span></span>
<span data-ttu-id="0045f-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0045f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0045f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0045f-126">-WhatIf</span></span>
<span data-ttu-id="0045f-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0045f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0045f-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0045f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0045f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0045f-129">CommonParameters</span></span>
<span data-ttu-id="0045f-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0045f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0045f-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0045f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0045f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0045f-132">INPUTS</span></span>

### <span data-ttu-id="0045f-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0045f-133">System.Guid</span></span>

### <span data-ttu-id="0045f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0045f-134">System.String</span></span>

## <span data-ttu-id="0045f-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0045f-135">OUTPUTS</span></span>

### <span data-ttu-id="0045f-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="0045f-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="0045f-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0045f-137">NOTES</span></span>

## <span data-ttu-id="0045f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0045f-138">RELATED LINKS</span></span>

[<span data-ttu-id="0045f-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0045f-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="0045f-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0045f-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="0045f-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="0045f-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



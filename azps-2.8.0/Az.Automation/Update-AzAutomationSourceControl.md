---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: 7786431232f9570557593d2fbdde65a21e34f9bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667709"
---
# <span data-ttu-id="024bb-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="024bb-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="024bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="024bb-102">SYNOPSIS</span></span>
<span data-ttu-id="024bb-103">Az Azure automatizálási adatforrás vezérlőjének frissítése</span><span class="sxs-lookup"><span data-stu-id="024bb-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="024bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="024bb-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="024bb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="024bb-105">DESCRIPTION</span></span>
<span data-ttu-id="024bb-106">A Update-AzAutomationSourceControl parancsmag az Azure automatizálási szolgáltatásban egy mező értékének értékét módosítja.</span><span class="sxs-lookup"><span data-stu-id="024bb-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="024bb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="024bb-107">EXAMPLES</span></span>

### <span data-ttu-id="024bb-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="024bb-108">Example 1</span></span>
<span data-ttu-id="024bb-109">Ez a parancs a PublishRunbook mezőt false értékre állítja az Azure automatizálási VSTSNative nevű devAccount nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="024bb-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="024bb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="024bb-110">PARAMETERS</span></span>

### <span data-ttu-id="024bb-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="024bb-111">-AccessToken</span></span>
<span data-ttu-id="024bb-112">A Forrásobjektum-hozzáférési jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="024bb-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bb-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="024bb-113">-AutomationAccountName</span></span>
<span data-ttu-id="024bb-114">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="024bb-114">The automation account name.</span></span>

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

### <span data-ttu-id="024bb-115">-AutoSync</span><span class="sxs-lookup"><span data-stu-id="024bb-115">-AutoSync</span></span>
<span data-ttu-id="024bb-116">A verziókövetés AutoSync tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="024bb-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bb-117">-Branch</span><span class="sxs-lookup"><span data-stu-id="024bb-117">-Branch</span></span>
<span data-ttu-id="024bb-118">A forrás vezérlő ágat.</span><span class="sxs-lookup"><span data-stu-id="024bb-118">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="024bb-119">-DefaultProfile</span></span>
<span data-ttu-id="024bb-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="024bb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="024bb-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="024bb-121">-Description</span></span>
<span data-ttu-id="024bb-122">A forrás vezérlő leírása.</span><span class="sxs-lookup"><span data-stu-id="024bb-122">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bb-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="024bb-123">-FolderPath</span></span>
<span data-ttu-id="024bb-124">A verziókövetés mappa elérési útja.</span><span class="sxs-lookup"><span data-stu-id="024bb-124">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bb-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="024bb-125">-Name</span></span>
<span data-ttu-id="024bb-126">A forrás vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="024bb-126">The source control name.</span></span>

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

### <span data-ttu-id="024bb-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="024bb-127">-PublishRunbook</span></span>
<span data-ttu-id="024bb-128">A verziókövetés publishRunbook tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="024bb-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="024bb-129">-ResourceGroupName</span></span>
<span data-ttu-id="024bb-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="024bb-130">The resource group name.</span></span>

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

### <span data-ttu-id="024bb-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="024bb-131">-Confirm</span></span>
<span data-ttu-id="024bb-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="024bb-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="024bb-133">-WhatIf</span></span>
<span data-ttu-id="024bb-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="024bb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="024bb-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="024bb-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="024bb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="024bb-136">CommonParameters</span></span>
<span data-ttu-id="024bb-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="024bb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="024bb-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="024bb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="024bb-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="024bb-139">INPUTS</span></span>

### <span data-ttu-id="024bb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="024bb-140">System.String</span></span>

## <span data-ttu-id="024bb-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="024bb-141">OUTPUTS</span></span>

### <span data-ttu-id="024bb-142">Microsoft. Azure. Command. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="024bb-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="024bb-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="024bb-143">NOTES</span></span>

## <span data-ttu-id="024bb-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="024bb-144">RELATED LINKS</span></span>

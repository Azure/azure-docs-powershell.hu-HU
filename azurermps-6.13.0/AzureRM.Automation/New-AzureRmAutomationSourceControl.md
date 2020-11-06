---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSourceControl.md
ms.openlocfilehash: d81d62e6ba391fb601817544d977f56e75522ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498491"
---
# <span data-ttu-id="7ea25-101">New-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="7ea25-101">New-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="7ea25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ea25-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea25-103">Automatizálási adatforrás-vezérlőt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7ea25-103">Creates an A Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ea25-104">SYNTAX</span></span>

```
New-AzureRmAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String>
 -AccessToken <SecureString> -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync]
 [-DoNotPublishRunbook] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ea25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ea25-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea25-106">Az New-AzureRmAutomationSourceControl parancsmag egy olyan konfigurációt hoz létre, amellyel az Azure automatizálási fiókját az VSTS-TFVC, a git vagy a GitHub VSTS kapcsolja össze.</span><span class="sxs-lookup"><span data-stu-id="7ea25-106">The New-AzureRmAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="7ea25-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7ea25-107">EXAMPLES</span></span>

### <span data-ttu-id="7ea25-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ea25-108">Example 1</span></span>
<span data-ttu-id="7ea25-109">Adatforrás-vezérlő konfiguráció létrehozása az Azure automatizálási fióknak a saját VSTS TFVC projekthez való csatolásához.</span><span class="sxs-lookup"><span data-stu-id="7ea25-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="7ea25-110">Az TFVC-projekteknek nincsenek ágai, ezért a Branch paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="7ea25-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="7ea25-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="7ea25-111">Example 2</span></span>
<span data-ttu-id="7ea25-112">A verziókövetés konfigurációjának létrehozásával az Azure automatizálási fiókját összekapcsolhatja a saját VSTS git Project segítségével.</span><span class="sxs-lookup"><span data-stu-id="7ea25-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="7ea25-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="7ea25-113">Example 3</span></span>
<span data-ttu-id="7ea25-114">Adatforrás-vezérlő konfiguráció létrehozása az Azure automatizálási fióknak a GitHub projectkel való összekapcsolásához</span><span class="sxs-lookup"><span data-stu-id="7ea25-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="7ea25-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ea25-115">PARAMETERS</span></span>

### <span data-ttu-id="7ea25-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="7ea25-116">-AccessToken</span></span>
<span data-ttu-id="7ea25-117">A Forrásobjektum-hozzáférési jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="7ea25-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea25-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7ea25-118">-AutomationAccountName</span></span>
<span data-ttu-id="7ea25-119">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="7ea25-119">The automation account name.</span></span>

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

### <span data-ttu-id="7ea25-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="7ea25-120">-Branch</span></span>
<span data-ttu-id="7ea25-121">A forrás vezérlő ágat.</span><span class="sxs-lookup"><span data-stu-id="7ea25-121">The source control branch.</span></span>

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

### <span data-ttu-id="7ea25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea25-122">-DefaultProfile</span></span>
<span data-ttu-id="7ea25-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ea25-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea25-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7ea25-124">-Description</span></span>
<span data-ttu-id="7ea25-125">A forrás vezérlő leírása.</span><span class="sxs-lookup"><span data-stu-id="7ea25-125">The source control description.</span></span>

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

### <span data-ttu-id="7ea25-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="7ea25-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="7ea25-127">A verziókövetés publishRunbook tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="7ea25-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="7ea25-128">Ha a DoNotPublishRunbook be van állítva, az azt jelenti, hogy a felhasználói runbooks "piszkozatként" lesz importálva.</span><span class="sxs-lookup"><span data-stu-id="7ea25-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea25-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="7ea25-129">-EnableAutoSync</span></span>
<span data-ttu-id="7ea25-130">A verziókövetés AutoSync tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="7ea25-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea25-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="7ea25-131">-FolderPath</span></span>
<span data-ttu-id="7ea25-132">A verziókövetés mappa elérési útja.</span><span class="sxs-lookup"><span data-stu-id="7ea25-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea25-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ea25-133">-Name</span></span>
<span data-ttu-id="7ea25-134">A forrás vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="7ea25-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea25-135">-Kiöntés</span><span class="sxs-lookup"><span data-stu-id="7ea25-135">-RepoUrl</span></span>
<span data-ttu-id="7ea25-136">A verziókövetés repó URL-címe.</span><span class="sxs-lookup"><span data-stu-id="7ea25-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea25-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea25-137">-ResourceGroupName</span></span>
<span data-ttu-id="7ea25-138">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ea25-138">The resource group name.</span></span>

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

### <span data-ttu-id="7ea25-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="7ea25-139">-SourceType</span></span>
<span data-ttu-id="7ea25-140">A forrás vezérlőelem típusa.</span><span class="sxs-lookup"><span data-stu-id="7ea25-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea25-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ea25-141">-Confirm</span></span>
<span data-ttu-id="7ea25-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ea25-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea25-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea25-143">-WhatIf</span></span>
<span data-ttu-id="7ea25-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ea25-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea25-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ea25-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ea25-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea25-146">CommonParameters</span></span>
<span data-ttu-id="7ea25-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ea25-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea25-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea25-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea25-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ea25-149">INPUTS</span></span>

### <span data-ttu-id="7ea25-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea25-150">System.String</span></span>

## <span data-ttu-id="7ea25-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ea25-151">OUTPUTS</span></span>

### <span data-ttu-id="7ea25-152">Microsoft. Azure. Command. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="7ea25-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="7ea25-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ea25-153">NOTES</span></span>

## <span data-ttu-id="7ea25-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ea25-154">RELATED LINKS</span></span>

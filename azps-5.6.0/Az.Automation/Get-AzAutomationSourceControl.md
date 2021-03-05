---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 051eee1c191662e6ca4eb56e34088af651ea69f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014165"
---
# <span data-ttu-id="fbb6e-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="fbb6e-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="fbb6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb6e-103">Az Azure Automation forrásvezérlőinek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="fbb6e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fbb6e-104">SYNTAX</span></span>

### <span data-ttu-id="fbb6e-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbb6e-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbb6e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fbb6e-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbb6e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fbb6e-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb6e-108">A Get-AzAutomationSourceControl parancsmag automatizálási forrásvezérlőket kap.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="fbb6e-109">Ha egy adott forrásvezérlőt is be kell szereznie, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="fbb6e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fbb6e-110">EXAMPLES</span></span>

### <span data-ttu-id="fbb6e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fbb6e-111">Example 1</span></span>
<span data-ttu-id="fbb6e-112">Ez a parancs egy VSTSNative nevű automatizálási forrásvezérlőt kap a devAccount nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="fbb6e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb6e-113">PARAMETERS</span></span>

### <span data-ttu-id="fbb6e-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fbb6e-114">-AutomationAccountName</span></span>
<span data-ttu-id="fbb6e-115">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-115">The automation account name.</span></span>

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

### <span data-ttu-id="fbb6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb6e-116">-DefaultProfile</span></span>
<span data-ttu-id="fbb6e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb6e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fbb6e-118">-Name</span></span>
<span data-ttu-id="fbb6e-119">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb6e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb6e-120">-ResourceGroupName</span></span>
<span data-ttu-id="fbb6e-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-121">The resource group name.</span></span>

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

### <span data-ttu-id="fbb6e-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="fbb6e-122">-SourceType</span></span>
<span data-ttu-id="fbb6e-123">A forrásvezérlő típusa.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb6e-124">CommonParameters</span></span>
<span data-ttu-id="fbb6e-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb6e-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb6e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb6e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbb6e-127">INPUTS</span></span>

### <span data-ttu-id="fbb6e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fbb6e-128">System.String</span></span>

## <span data-ttu-id="fbb6e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb6e-129">OUTPUTS</span></span>

### <span data-ttu-id="fbb6e-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="fbb6e-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="fbb6e-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fbb6e-131">NOTES</span></span>

## <span data-ttu-id="fbb6e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbb6e-132">RELATED LINKS</span></span>

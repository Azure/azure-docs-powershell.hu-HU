---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 3e7affd09e8c24c1d3c1759e78ea09a0c849ff32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501216"
---
# <span data-ttu-id="e6ad4-101">Get-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="e6ad4-101">Get-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="e6ad4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ad4-103">Beolvassa az Azure automatizálási vezérlők listáját.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-103">Gets a list of Azure Automation source controls.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6ad4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6ad4-104">SYNTAX</span></span>

### <span data-ttu-id="e6ad4-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6ad4-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6ad4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e6ad4-106">ByName</span></span>
```
Get-AzureRmAutomationSourceControl -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6ad4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6ad4-107">DESCRIPTION</span></span>
<span data-ttu-id="e6ad4-108">Az Get-AzureRmAutomationSourceControl parancsmag automatizálási adatforrás-vezérlőket kap.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-108">The Get-AzureRmAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="e6ad4-109">Ha egy konkrét forrás vezérlőt szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="e6ad4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e6ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="e6ad4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6ad4-111">Example 1</span></span>
<span data-ttu-id="e6ad4-112">Ez a parancs egy VSTSNative nevű automatizálási vezérlőt kap a devAccount nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="e6ad4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6ad4-113">PARAMETERS</span></span>

### <span data-ttu-id="e6ad4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e6ad4-114">-AutomationAccountName</span></span>
<span data-ttu-id="e6ad4-115">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-115">The automation account name.</span></span>

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

### <span data-ttu-id="e6ad4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ad4-116">-DefaultProfile</span></span>
<span data-ttu-id="e6ad4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ad4-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6ad4-118">-Name</span></span>
<span data-ttu-id="e6ad4-119">A forrás vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-119">The source control name.</span></span>

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

### <span data-ttu-id="e6ad4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ad4-120">-ResourceGroupName</span></span>
<span data-ttu-id="e6ad4-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-121">The resource group name.</span></span>

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

### <span data-ttu-id="e6ad4-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="e6ad4-122">-SourceType</span></span>
<span data-ttu-id="e6ad4-123">A forrás vezérlőelem típusa.</span><span class="sxs-lookup"><span data-stu-id="e6ad4-123">The source control type.</span></span>

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

### <span data-ttu-id="e6ad4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ad4-124">CommonParameters</span></span>
<span data-ttu-id="e6ad4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6ad4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ad4-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ad4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ad4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ad4-127">INPUTS</span></span>

### <span data-ttu-id="e6ad4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e6ad4-128">System.String</span></span>

## <span data-ttu-id="e6ad4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ad4-129">OUTPUTS</span></span>

### <span data-ttu-id="e6ad4-130">Microsoft. Azure. Command. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="e6ad4-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="e6ad4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6ad4-131">NOTES</span></span>

## <span data-ttu-id="e6ad4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6ad4-132">RELATED LINKS</span></span>

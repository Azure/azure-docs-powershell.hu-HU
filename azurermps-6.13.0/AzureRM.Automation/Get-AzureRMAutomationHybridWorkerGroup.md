---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 8fe4c554fd781d198af6bea784a433c141c2d41d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679629"
---
# <span data-ttu-id="fdafb-101">Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="fdafb-101">Get-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="fdafb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdafb-102">SYNOPSIS</span></span>
<span data-ttu-id="fdafb-103">Hibrid runbook-munkavégző csoportokba kerül.</span><span class="sxs-lookup"><span data-stu-id="fdafb-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdafb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdafb-104">SYNTAX</span></span>

### <span data-ttu-id="fdafb-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdafb-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdafb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fdafb-106">ByName</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdafb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdafb-107">DESCRIPTION</span></span>
<span data-ttu-id="fdafb-108">A **Get-AzureRmAutomationHybridWorkerGroup** parancsmag Azure Automation hibrid runbook-munkacsoportokat kap.</span><span class="sxs-lookup"><span data-stu-id="fdafb-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="fdafb-109">Ha meghatározott csoportot szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="fdafb-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="fdafb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fdafb-110">EXAMPLES</span></span>

### <span data-ttu-id="fdafb-111">Példa 1: az összes hibrid runbook munkatársi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="fdafb-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="fdafb-112">Ez a parancs a Contoso17 nevű automatizálási fiók minden hibrid runbook bekerül.</span><span class="sxs-lookup"><span data-stu-id="fdafb-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="fdafb-113">2. példa: egyetlen hibrid runbook-munkatársi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="fdafb-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="fdafb-114">Ez a parancs a Contoso17 nevű automatizálási fiók HybridRunbookWorkerGroup01 nevű hibrid runbook-csoportját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fdafb-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="fdafb-115">3. példa: a munkavállalók beszerzése hibrid runbook-csoportba</span><span class="sxs-lookup"><span data-stu-id="fdafb-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="fdafb-116">Ez a parancs a Contoso17 nevű runbook nevű runbook a HybridRunbookWorkerGroup01 nevű hibrid-munkatársait kapja.</span><span class="sxs-lookup"><span data-stu-id="fdafb-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="fdafb-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdafb-117">PARAMETERS</span></span>

### <span data-ttu-id="fdafb-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fdafb-118">-AutomationAccountName</span></span>
<span data-ttu-id="fdafb-119">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdafb-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="fdafb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdafb-120">-DefaultProfile</span></span>
<span data-ttu-id="fdafb-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fdafb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdafb-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fdafb-122">-Name</span></span>
<span data-ttu-id="fdafb-123">A hibrid runbook a munkatársi csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdafb-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdafb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdafb-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdafb-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fdafb-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fdafb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdafb-126">CommonParameters</span></span>
<span data-ttu-id="fdafb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdafb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdafb-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdafb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdafb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdafb-129">INPUTS</span></span>

### <span data-ttu-id="fdafb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fdafb-130">System.String</span></span>
<span data-ttu-id="fdafb-131">Paraméterek: név (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fdafb-131">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="fdafb-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdafb-132">OUTPUTS</span></span>

### <span data-ttu-id="fdafb-133">Microsoft. Azure. Command. Automation. Model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="fdafb-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="fdafb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdafb-134">NOTES</span></span>

## <span data-ttu-id="fdafb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdafb-135">RELATED LINKS</span></span>

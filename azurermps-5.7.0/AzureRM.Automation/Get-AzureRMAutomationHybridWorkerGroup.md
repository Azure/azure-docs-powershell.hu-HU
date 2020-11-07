---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 4fd6ce26df8eeecc848f813e33cb867a412bbc8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672044"
---
# <span data-ttu-id="827c9-101">Get-AzureRMAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="827c9-101">Get-AzureRMAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="827c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="827c9-102">SYNOPSIS</span></span>
<span data-ttu-id="827c9-103">Hibrid runbook-munkavégző csoportokba kerül.</span><span class="sxs-lookup"><span data-stu-id="827c9-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="827c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="827c9-104">SYNTAX</span></span>

### <span data-ttu-id="827c9-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="827c9-105">ByAll (Default)</span></span>
```
Get-AzureRMAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="827c9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="827c9-106">ByName</span></span>
```
Get-AzureRMAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="827c9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="827c9-107">DESCRIPTION</span></span>
<span data-ttu-id="827c9-108">A **Get-AzureRmAutomationHybridWorkerGroup** parancsmag Azure Automation hibrid runbook-munkacsoportokat kap.</span><span class="sxs-lookup"><span data-stu-id="827c9-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="827c9-109">Ha meghatározott csoportot szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="827c9-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="827c9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="827c9-110">EXAMPLES</span></span>

### <span data-ttu-id="827c9-111">Példa 1: az összes hibrid runbook munkatársi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="827c9-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="827c9-112">Ez a parancs a Contoso17 nevű automatizálási fiók minden hibrid runbook bekerül.</span><span class="sxs-lookup"><span data-stu-id="827c9-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="827c9-113">2. példa: egyetlen hibrid runbook-munkatársi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="827c9-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="827c9-114">Ez a parancs a Contoso17 nevű automatizálási fiók HybridRunbookWorkerGroup01 nevű hibrid runbook-csoportját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="827c9-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="827c9-115">3. példa: a munkavállalók beszerzése hibrid runbook-csoportba</span><span class="sxs-lookup"><span data-stu-id="827c9-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="827c9-116">Ez a parancs a Contoso17 nevű runbook nevű runbook a HybridRunbookWorkerGroup01 nevű hibrid-munkatársait kapja.</span><span class="sxs-lookup"><span data-stu-id="827c9-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="827c9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="827c9-117">PARAMETERS</span></span>

### <span data-ttu-id="827c9-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="827c9-118">-AutomationAccountName</span></span>
<span data-ttu-id="827c9-119">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="827c9-119">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="827c9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827c9-120">-DefaultProfile</span></span>
<span data-ttu-id="827c9-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="827c9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="827c9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="827c9-122">-Name</span></span>
<span data-ttu-id="827c9-123">A hibrid runbook a munkatársi csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="827c9-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="827c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="827c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="827c9-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="827c9-125">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="827c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827c9-126">CommonParameters</span></span>
<span data-ttu-id="827c9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="827c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827c9-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827c9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="827c9-129">INPUTS</span></span>

### <span data-ttu-id="827c9-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="827c9-130">String</span></span>
<span data-ttu-id="827c9-131">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="827c9-131">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="827c9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="827c9-132">OUTPUTS</span></span>

### <span data-ttu-id="827c9-133">Microsoft. Azure. Command. Automation. Model. HybridRunbookWorker</span><span class="sxs-lookup"><span data-stu-id="827c9-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorker</span></span>

## <span data-ttu-id="827c9-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="827c9-134">NOTES</span></span>

## <span data-ttu-id="827c9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="827c9-135">RELATED LINKS</span></span>


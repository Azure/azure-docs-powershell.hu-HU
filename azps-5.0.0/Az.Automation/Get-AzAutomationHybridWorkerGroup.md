---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186434"
---
# <span data-ttu-id="bc1bd-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="bc1bd-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="bc1bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="bc1bd-103">Hibrid runbook-munkavégző csoportokba kerül.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="bc1bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc1bd-104">SYNTAX</span></span>

### <span data-ttu-id="bc1bd-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc1bd-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc1bd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bc1bd-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc1bd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc1bd-107">DESCRIPTION</span></span>
<span data-ttu-id="bc1bd-108">A **Get-AzAutomationHybridWorkerGroup** parancsmag Azure Automation hibrid runbook-munkacsoportokat kap.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="bc1bd-109">Ha meghatározott csoportot szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="bc1bd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bc1bd-110">EXAMPLES</span></span>

### <span data-ttu-id="bc1bd-111">Példa 1: az összes hibrid runbook munkatársi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="bc1bd-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="bc1bd-112">Ez a parancs a Contoso17 nevű automatizálási fiók minden hibrid runbook bekerül.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bc1bd-113">2. példa: egyetlen hibrid runbook-munkatársi csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="bc1bd-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="bc1bd-114">Ez a parancs a Contoso17 nevű automatizálási fiók HybridRunbookWorkerGroup01 nevű hibrid runbook-csoportját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bc1bd-115">3. példa: a munkavállalók beszerzése hibrid runbook-csoportba</span><span class="sxs-lookup"><span data-stu-id="bc1bd-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="bc1bd-116">Ez a parancs a Contoso17 nevű runbook nevű runbook a HybridRunbookWorkerGroup01 nevű hibrid-munkatársait kapja.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="bc1bd-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc1bd-117">PARAMETERS</span></span>

### <span data-ttu-id="bc1bd-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc1bd-118">-AutomationAccountName</span></span>
<span data-ttu-id="bc1bd-119">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="bc1bd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc1bd-120">-DefaultProfile</span></span>
<span data-ttu-id="bc1bd-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bc1bd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc1bd-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc1bd-122">-Name</span></span>
<span data-ttu-id="bc1bd-123">A hibrid runbook a munkatársi csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="bc1bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc1bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc1bd-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bc1bd-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bc1bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc1bd-126">CommonParameters</span></span>
<span data-ttu-id="bc1bd-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc1bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc1bd-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc1bd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc1bd-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc1bd-129">INPUTS</span></span>

### <span data-ttu-id="bc1bd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bc1bd-130">System.String</span></span>

## <span data-ttu-id="bc1bd-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc1bd-131">OUTPUTS</span></span>

### <span data-ttu-id="bc1bd-132">Microsoft. Azure. Command. Automation. Model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="bc1bd-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="bc1bd-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc1bd-133">NOTES</span></span>

## <span data-ttu-id="bc1bd-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc1bd-134">RELATED LINKS</span></span>
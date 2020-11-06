---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 0820905ff8a4673c9abae56be2f7792912095e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495172"
---
# <span data-ttu-id="34737-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="34737-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="34737-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34737-102">SYNOPSIS</span></span>
<span data-ttu-id="34737-103">Egy automatizálási feladat felfüggesztése.</span><span class="sxs-lookup"><span data-stu-id="34737-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34737-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34737-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34737-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="34737-105">DESCRIPTION</span></span>
<span data-ttu-id="34737-106">A **felfüggesztés – AzureRmAutomationJob** parancsmag felfüggeszti az Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="34737-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="34737-107">Adja meg a futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="34737-107">Specify a running Automation job.</span></span>
<span data-ttu-id="34737-108">Felfüggesztett feladat folytatásához használja az Resume-AzureRmAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="34737-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="34737-109">Példák</span><span class="sxs-lookup"><span data-stu-id="34737-109">EXAMPLES</span></span>

### <span data-ttu-id="34737-110">1. példa: feladat felfüggesztése</span><span class="sxs-lookup"><span data-stu-id="34737-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="34737-111">Ez a parancs felfüggeszti a megadott azonosítót tartalmazó feladatot.</span><span class="sxs-lookup"><span data-stu-id="34737-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="34737-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34737-112">PARAMETERS</span></span>

### <span data-ttu-id="34737-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="34737-113">-AutomationAccountName</span></span>
<span data-ttu-id="34737-114">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag felfüggeszti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="34737-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="34737-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34737-115">-DefaultProfile</span></span>
<span data-ttu-id="34737-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="34737-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34737-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="34737-117">-Id</span></span>
<span data-ttu-id="34737-118">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="34737-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34737-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34737-119">-ResourceGroupName</span></span>
<span data-ttu-id="34737-120">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag felfüggeszti.</span><span class="sxs-lookup"><span data-stu-id="34737-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="34737-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34737-121">CommonParameters</span></span>
<span data-ttu-id="34737-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34737-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34737-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34737-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34737-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34737-124">INPUTS</span></span>

### <span data-ttu-id="34737-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="34737-125">System.Guid</span></span>

### <span data-ttu-id="34737-126">System. String</span><span class="sxs-lookup"><span data-stu-id="34737-126">System.String</span></span>

## <span data-ttu-id="34737-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34737-127">OUTPUTS</span></span>

### <span data-ttu-id="34737-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="34737-128">System.Void</span></span>

## <span data-ttu-id="34737-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34737-129">NOTES</span></span>

## <span data-ttu-id="34737-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34737-130">RELATED LINKS</span></span>

[<span data-ttu-id="34737-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="34737-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="34737-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="34737-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="34737-133">Önéletrajz – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="34737-133">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="34737-134">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="34737-134">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)



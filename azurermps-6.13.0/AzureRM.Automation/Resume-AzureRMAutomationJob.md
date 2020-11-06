---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 8e84f2f66703410b626769be8c2c2d5a57e531e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494188"
---
# <span data-ttu-id="1ae97-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1ae97-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="1ae97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ae97-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae97-103">Befejezi a felfüggesztett automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ae97-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ae97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ae97-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae97-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ae97-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae97-106">A **resume-AzureRmAutomationJob** parancsmag felfüggesztette az Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ae97-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="1ae97-107">Adja meg a felfüggesztett feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ae97-107">Specify the suspended job.</span></span>
<span data-ttu-id="1ae97-108">A feladat felfüggesztéséhez használja az Suspend-AzureRmAutomationJob parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1ae97-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="1ae97-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1ae97-109">EXAMPLES</span></span>

### <span data-ttu-id="1ae97-110">1. példa: felfüggesztett feladat folytatása</span><span class="sxs-lookup"><span data-stu-id="1ae97-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1ae97-111">Ez a parancs folytatja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="1ae97-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="1ae97-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ae97-112">PARAMETERS</span></span>

### <span data-ttu-id="1ae97-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ae97-113">-AutomationAccountName</span></span>
<span data-ttu-id="1ae97-114">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag folytatja a munkát.</span><span class="sxs-lookup"><span data-stu-id="1ae97-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="1ae97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae97-115">-DefaultProfile</span></span>
<span data-ttu-id="1ae97-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1ae97-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ae97-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="1ae97-117">-Id</span></span>
<span data-ttu-id="1ae97-118">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag visszatér.</span><span class="sxs-lookup"><span data-stu-id="1ae97-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="1ae97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae97-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ae97-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag folytatja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="1ae97-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="1ae97-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae97-121">CommonParameters</span></span>
<span data-ttu-id="1ae97-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ae97-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae97-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae97-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae97-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ae97-124">INPUTS</span></span>

### <span data-ttu-id="1ae97-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1ae97-125">System.Guid</span></span>

### <span data-ttu-id="1ae97-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae97-126">System.String</span></span>

## <span data-ttu-id="1ae97-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ae97-127">OUTPUTS</span></span>

### <span data-ttu-id="1ae97-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="1ae97-128">System.Void</span></span>

## <span data-ttu-id="1ae97-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ae97-129">NOTES</span></span>

## <span data-ttu-id="1ae97-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ae97-130">RELATED LINKS</span></span>

[<span data-ttu-id="1ae97-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1ae97-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="1ae97-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1ae97-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="1ae97-133">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1ae97-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="1ae97-134">Felfüggesztés – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1ae97-134">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)



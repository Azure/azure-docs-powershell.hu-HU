---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: a7ddc25fa7c6bc52acbe9369c569db060cf63a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492045"
---
# <span data-ttu-id="b45f3-101">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b45f3-101">Get-AzureRmAutomationDscCompilationJobOutput</span></span>

## <span data-ttu-id="b45f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b45f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b45f3-103">Egy automatizálási DSC összeállítási feladat naplózási folyamait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b45f3-103">Gets the logging streams of an Automation DSC compilation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b45f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b45f3-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b45f3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b45f3-105">DESCRIPTION</span></span>
<span data-ttu-id="b45f3-106">A **Get-AzureRmAutomationDscCompilationJobOutput** PARANCSMAG a APS-alapú szükséges állapot-konfiguráció (DSC) fordítási feladatának stream-rekordjait kapja meg az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="b45f3-106">The **Get-AzureRmAutomationDscCompilationJobOutput** cmdlet gets the stream records of an APS Desired State Configuration (DSC) compilation job in Azure Automation.</span></span>

## <span data-ttu-id="b45f3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b45f3-107">EXAMPLES</span></span>

### <span data-ttu-id="b45f3-108">Példa 1: a DSC-összeállítási feladathoz tartozó naplók beszerzése</span><span class="sxs-lookup"><span data-stu-id="b45f3-108">Example 1: Get the logs for a DSC compilation job</span></span>
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

<span data-ttu-id="b45f3-109">Az első parancs a fordítási feladatokat a Contoso17 nevű automatizálási fiókból kapja meg az Get-AzureRmAutomationDscCompilationJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b45f3-109">The first command gets the compilation jobs in the Automation account named Contoso17 by using the Get-AzureRmAutomationDscCompilationJob cmdlet.</span></span>
<span data-ttu-id="b45f3-110">A parancs ezeket az objektumokat a $Jobs változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b45f3-110">The command stores those objects in the $Jobs variable.</span></span>
<span data-ttu-id="b45f3-111">A második parancs beolvassa a fordítási munka kimenetét a $Jobs tömb első tagjának minden adatfolyamhoz.</span><span class="sxs-lookup"><span data-stu-id="b45f3-111">The second command gets the compilation job output for any stream for the first member of the $Jobs array.</span></span>

## <span data-ttu-id="b45f3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b45f3-112">PARAMETERS</span></span>

### <span data-ttu-id="b45f3-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b45f3-113">-AutomationAccountName</span></span>
<span data-ttu-id="b45f3-114">A DSC összeállítási feladatot tartalmazó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b45f3-114">Specifies the name of the Automation account that contains the DSC compilation job.</span></span>

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

### <span data-ttu-id="b45f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45f3-115">-DefaultProfile</span></span>
<span data-ttu-id="b45f3-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b45f3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b45f3-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b45f3-117">-Id</span></span>
<span data-ttu-id="b45f3-118">Megadja annak a DSC-összeállításnak az egyedi AZONOSÍTÓját, amelyre a parancsmag kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="b45f3-118">Specifies the unique ID of the DSC compilation job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="b45f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b45f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="b45f3-120">Annak a DSC-összeállítási feladatot tartalmazó erőforráscsoportnak a nevét adja meg, amelyhez ez a parancsmag adatfolyam-nyilvántartást kap.</span><span class="sxs-lookup"><span data-stu-id="b45f3-120">Specifies the name of the resource group that contains the DSC compilation job for which this cmdlet gets stream records.</span></span>

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

### <span data-ttu-id="b45f3-121">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="b45f3-121">-StartTime</span></span>
<span data-ttu-id="b45f3-122">Megadja a kezdés időpontját.</span><span class="sxs-lookup"><span data-stu-id="b45f3-122">Specifies a start time.</span></span>
<span data-ttu-id="b45f3-123">Ez a parancsmag olyan adatfolyam-rekordokat kap, amelyekben a DSC fordítási feladat az adott időpont után kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="b45f3-123">This cmdlet gets stream records that the DSC compilation job outputs after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b45f3-124">-Stream</span><span class="sxs-lookup"><span data-stu-id="b45f3-124">-Stream</span></span>
<span data-ttu-id="b45f3-125">Annak a kimenetnek az adatfolyam-típusát adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="b45f3-125">Specifies the type of stream for the output that this cmdlet gets.</span></span>
<span data-ttu-id="b45f3-126">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="b45f3-126">Valid values are:</span></span> 
- <span data-ttu-id="b45f3-127">Bármely</span><span class="sxs-lookup"><span data-stu-id="b45f3-127">Any</span></span> 
- <span data-ttu-id="b45f3-128">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="b45f3-128">Warning</span></span> 
- <span data-ttu-id="b45f3-129">Hiba</span><span class="sxs-lookup"><span data-stu-id="b45f3-129">Error</span></span> 
- <span data-ttu-id="b45f3-130">Részletes</span><span class="sxs-lookup"><span data-stu-id="b45f3-130">Verbose</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b45f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45f3-131">CommonParameters</span></span>
<span data-ttu-id="b45f3-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b45f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b45f3-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b45f3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45f3-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b45f3-134">INPUTS</span></span>

### <span data-ttu-id="b45f3-135">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b45f3-135">System.Guid</span></span>

### <span data-ttu-id="b45f3-136">Microsoft. Azure. Command. Automation. Common. CompilationJobStreamType</span><span class="sxs-lookup"><span data-stu-id="b45f3-136">Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType</span></span>

### <span data-ttu-id="b45f3-137">System. null ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b45f3-137">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b45f3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b45f3-138">System.String</span></span>

## <span data-ttu-id="b45f3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b45f3-139">OUTPUTS</span></span>

### <span data-ttu-id="b45f3-140">Microsoft. Azure. Command. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="b45f3-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="b45f3-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b45f3-141">NOTES</span></span>

## <span data-ttu-id="b45f3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b45f3-142">RELATED LINKS</span></span>

[<span data-ttu-id="b45f3-143">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b45f3-143">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="b45f3-144">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b45f3-144">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)



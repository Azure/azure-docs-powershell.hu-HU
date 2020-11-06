---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: db7e76a21f635429be598ca9f40899ece3fa0406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503275"
---
# <span data-ttu-id="38af3-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="38af3-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="38af3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38af3-102">SYNOPSIS</span></span>
<span data-ttu-id="38af3-103">Automatizálási feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="38af3-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38af3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38af3-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38af3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38af3-105">DESCRIPTION</span></span>
<span data-ttu-id="38af3-106">A **stop-AzureRmAutomationJob** parancsmag leállítja az Azure automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="38af3-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="38af3-107">Adja meg a futó automatizálási feladatot.</span><span class="sxs-lookup"><span data-stu-id="38af3-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="38af3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="38af3-108">EXAMPLES</span></span>

### <span data-ttu-id="38af3-109">Példa 1: feladat leállítása</span><span class="sxs-lookup"><span data-stu-id="38af3-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="38af3-110">Ez a parancs leállítja a megadott azonosítót tartalmazó munkát.</span><span class="sxs-lookup"><span data-stu-id="38af3-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="38af3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38af3-111">PARAMETERS</span></span>

### <span data-ttu-id="38af3-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38af3-112">-AutomationAccountName</span></span>
<span data-ttu-id="38af3-113">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag leállítja a feladatot.</span><span class="sxs-lookup"><span data-stu-id="38af3-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="38af3-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="38af3-114">-Id</span></span>
<span data-ttu-id="38af3-115">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag leáll.</span><span class="sxs-lookup"><span data-stu-id="38af3-115">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="38af3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38af3-116">-ResourceGroupName</span></span>
<span data-ttu-id="38af3-117">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38af3-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="38af3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38af3-118">-DefaultProfile</span></span>
<span data-ttu-id="38af3-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38af3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38af3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38af3-120">CommonParameters</span></span>
<span data-ttu-id="38af3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38af3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38af3-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38af3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38af3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38af3-123">INPUTS</span></span>

## <span data-ttu-id="38af3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38af3-124">OUTPUTS</span></span>

## <span data-ttu-id="38af3-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38af3-125">NOTES</span></span>

## <span data-ttu-id="38af3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38af3-126">RELATED LINKS</span></span>

[<span data-ttu-id="38af3-127">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="38af3-127">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="38af3-128">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="38af3-128">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="38af3-129">Önéletrajz – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="38af3-129">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="38af3-130">Felfüggesztés – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="38af3-130">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015611"
---
# <span data-ttu-id="95ba3-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="95ba3-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="95ba3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="95ba3-103">Elérhetővé válik az ütemező helye.</span><span class="sxs-lookup"><span data-stu-id="95ba3-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="95ba3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95ba3-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="95ba3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95ba3-105">DESCRIPTION</span></span>
<span data-ttu-id="95ba3-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="95ba3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="95ba3-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="95ba3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="95ba3-108">A **Get-AzureSchedulerLocation** parancsmag elérhetővé válik az ütemező helyekkel.</span><span class="sxs-lookup"><span data-stu-id="95ba3-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="95ba3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="95ba3-109">EXAMPLES</span></span>

### <span data-ttu-id="95ba3-110">1. példa: az elérhető ütemező helyének beszerzése</span><span class="sxs-lookup"><span data-stu-id="95ba3-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="95ba3-111">A parancs elérhetővé válik az ütemező helyekkel.</span><span class="sxs-lookup"><span data-stu-id="95ba3-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="95ba3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95ba3-112">PARAMETERS</span></span>

### <span data-ttu-id="95ba3-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="95ba3-113">-Profile</span></span>
<span data-ttu-id="95ba3-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="95ba3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95ba3-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="95ba3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ba3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ba3-116">CommonParameters</span></span>
<span data-ttu-id="95ba3-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95ba3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ba3-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ba3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ba3-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95ba3-119">INPUTS</span></span>

## <span data-ttu-id="95ba3-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95ba3-120">OUTPUTS</span></span>

## <span data-ttu-id="95ba3-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95ba3-121">NOTES</span></span>

## <span data-ttu-id="95ba3-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95ba3-122">RELATED LINKS</span></span>

[<span data-ttu-id="95ba3-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="95ba3-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="95ba3-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="95ba3-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="95ba3-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="95ba3-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)



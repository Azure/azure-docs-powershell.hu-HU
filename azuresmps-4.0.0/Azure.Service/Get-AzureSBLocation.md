---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016312"
---
# <span data-ttu-id="f5eb3-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="f5eb3-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="f5eb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="f5eb3-103">A szolgáltatás Buszjának helyét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5eb3-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="f5eb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5eb3-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5eb3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="f5eb3-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="f5eb3-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f5eb3-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f5eb3-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f5eb3-108">A **Get-AzureSBLocation** parancsmag azokat a helyeket jeleníti meg, amelyekben a szolgáltatás busza elérhető.</span><span class="sxs-lookup"><span data-stu-id="f5eb3-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="f5eb3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f5eb3-109">EXAMPLES</span></span>

### <span data-ttu-id="f5eb3-110">Példa 1: a szolgáltatási busz helyének beszerzése</span><span class="sxs-lookup"><span data-stu-id="f5eb3-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="f5eb3-111">Ez a példa a szolgáltatás Buszjának helyét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f5eb3-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="f5eb3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5eb3-112">PARAMETERS</span></span>

### <span data-ttu-id="f5eb3-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="f5eb3-113">-Profile</span></span>
<span data-ttu-id="f5eb3-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f5eb3-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5eb3-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f5eb3-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5eb3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5eb3-116">CommonParameters</span></span>
<span data-ttu-id="f5eb3-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5eb3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5eb3-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5eb3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5eb3-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5eb3-119">INPUTS</span></span>

## <span data-ttu-id="f5eb3-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5eb3-120">OUTPUTS</span></span>

## <span data-ttu-id="f5eb3-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5eb3-121">NOTES</span></span>

## <span data-ttu-id="f5eb3-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5eb3-122">RELATED LINKS</span></span>

[<span data-ttu-id="f5eb3-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="f5eb3-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)



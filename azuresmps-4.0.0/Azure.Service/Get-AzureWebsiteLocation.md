---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016272"
---
# <span data-ttu-id="e9745-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="e9745-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="e9745-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9745-102">SYNOPSIS</span></span>
<span data-ttu-id="e9745-103">A rendelkezésre álló webhelyek minden helyének beolvasása.</span><span class="sxs-lookup"><span data-stu-id="e9745-103">Gets all available website locations.</span></span>

## <span data-ttu-id="e9745-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9745-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9745-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9745-105">DESCRIPTION</span></span>
<span data-ttu-id="e9745-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="e9745-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e9745-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e9745-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e9745-108">Az összes elérhető webhely helyének beolvasása az aktuális előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="e9745-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="e9745-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e9745-109">EXAMPLES</span></span>

### <span data-ttu-id="e9745-110">Példa 1: az összes elérhető hely beszerzése</span><span class="sxs-lookup"><span data-stu-id="e9745-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="e9745-111">Ez a példa a jelenlegi előfizetés összes elérhető webhelyét bekapja.</span><span class="sxs-lookup"><span data-stu-id="e9745-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="e9745-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9745-112">PARAMETERS</span></span>

### <span data-ttu-id="e9745-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="e9745-113">-Profile</span></span>
<span data-ttu-id="e9745-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e9745-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9745-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e9745-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9745-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9745-116">CommonParameters</span></span>
<span data-ttu-id="e9745-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9745-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9745-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9745-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9745-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9745-119">INPUTS</span></span>

## <span data-ttu-id="e9745-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9745-120">OUTPUTS</span></span>

## <span data-ttu-id="e9745-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9745-121">NOTES</span></span>

## <span data-ttu-id="e9745-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9745-122">RELATED LINKS</span></span>

[<span data-ttu-id="e9745-123">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e9745-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)



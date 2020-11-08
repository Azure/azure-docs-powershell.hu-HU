---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016335"
---
# <span data-ttu-id="b8cb4-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b8cb4-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="b8cb4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="b8cb4-103">Megkapja az elérhető Azure Media Services-fiókokat.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="b8cb4-104">**Megjegyzés:** Ez a verzió elavult, kérjük, olvassa el az [újabb verziót](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="b8cb4-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="b8cb4-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8cb4-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b8cb4-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8cb4-106">DESCRIPTION</span></span>
<span data-ttu-id="b8cb4-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b8cb4-108">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b8cb4-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b8cb4-109">Az összes fiók listázásához használja a `Get-AzureMediaServicesAccount` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="b8cb4-110">Ha részletesebb információt szeretne kapni egy adott fiókról, használja a `Get-AzureMediaServicesAccount -Name YourAccountName` parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="b8cb4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b8cb4-111">EXAMPLES</span></span>

### <span data-ttu-id="b8cb4-112">Példa 1: az összes Media Services-fiók listázása</span><span class="sxs-lookup"><span data-stu-id="b8cb4-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="b8cb4-113">Ez a parancs felsorolja az összes rendelkezésre álló Media Services-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="b8cb4-114">2. példa: részletes információk kérése a Media Services-fiókról</span><span class="sxs-lookup"><span data-stu-id="b8cb4-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="b8cb4-115">Ez a parancs a Media Services-fiók tulajdonságait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="b8cb4-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8cb4-116">PARAMETERS</span></span>

### <span data-ttu-id="b8cb4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8cb4-117">-Name</span></span>
<span data-ttu-id="b8cb4-118">A Media Services-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-118">The Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8cb4-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="b8cb4-119">-Profile</span></span>
<span data-ttu-id="b8cb4-120">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8cb4-121">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b8cb4-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b8cb4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8cb4-122">CommonParameters</span></span>
<span data-ttu-id="b8cb4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8cb4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8cb4-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8cb4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8cb4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8cb4-125">INPUTS</span></span>

## <span data-ttu-id="b8cb4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8cb4-126">OUTPUTS</span></span>

## <span data-ttu-id="b8cb4-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8cb4-127">NOTES</span></span>

## <span data-ttu-id="b8cb4-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8cb4-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8cb4-129">Az Azure PowerShell for Media Services használata</span><span class="sxs-lookup"><span data-stu-id="b8cb4-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)



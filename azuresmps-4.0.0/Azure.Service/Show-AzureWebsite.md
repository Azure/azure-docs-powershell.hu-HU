---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015785"
---
# <span data-ttu-id="12c56-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12c56-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="12c56-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12c56-102">SYNOPSIS</span></span>
<span data-ttu-id="12c56-103">Megnyit egy böngészőt egy adott webhelyen.</span><span class="sxs-lookup"><span data-stu-id="12c56-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="12c56-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12c56-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="12c56-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12c56-105">DESCRIPTION</span></span>
<span data-ttu-id="12c56-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="12c56-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="12c56-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="12c56-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="12c56-108">A **show-AzureWebsite** parancsmag megnyit egy böngészőt egy adott webhelyen.</span><span class="sxs-lookup"><span data-stu-id="12c56-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="12c56-109">Példák</span><span class="sxs-lookup"><span data-stu-id="12c56-109">EXAMPLES</span></span>

## <span data-ttu-id="12c56-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12c56-110">PARAMETERS</span></span>

### <span data-ttu-id="12c56-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12c56-111">-Name</span></span>
<span data-ttu-id="12c56-112">Annak a webhelynek a neve, amelyet meg szeretne nyitni a böngészőben.</span><span class="sxs-lookup"><span data-stu-id="12c56-112">Specifies the name of the site to open in the browser.</span></span>

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

### <span data-ttu-id="12c56-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="12c56-113">-Profile</span></span>
<span data-ttu-id="12c56-114">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="12c56-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12c56-115">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="12c56-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12c56-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="12c56-116">-Slot</span></span>
<span data-ttu-id="12c56-117">A webhely tárolóhelyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12c56-117">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="12c56-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c56-118">CommonParameters</span></span>
<span data-ttu-id="12c56-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12c56-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c56-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12c56-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c56-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12c56-121">INPUTS</span></span>

## <span data-ttu-id="12c56-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12c56-122">OUTPUTS</span></span>

## <span data-ttu-id="12c56-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12c56-123">NOTES</span></span>

## <span data-ttu-id="12c56-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12c56-124">RELATED LINKS</span></span>

[<span data-ttu-id="12c56-125">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="12c56-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="12c56-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12c56-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="12c56-127">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12c56-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="12c56-128">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12c56-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="12c56-129">Újraindítás – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12c56-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="12c56-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="12c56-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)



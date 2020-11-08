---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016001"
---
# <span data-ttu-id="6328c-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="6328c-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="6328c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6328c-102">SYNOPSIS</span></span>
<span data-ttu-id="6328c-103">Frissíti az Azure Media Services-fiók kulcsait.</span><span class="sxs-lookup"><span data-stu-id="6328c-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="6328c-104">**Megjegyzés:** Ez a verzió elavult, kérjük, olvassa el az [újabb verziót](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="6328c-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="6328c-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6328c-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6328c-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="6328c-106">DESCRIPTION</span></span>
<span data-ttu-id="6328c-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="6328c-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6328c-108">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6328c-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6328c-109">A **New-AzureMediaServicesKey** parancsmag frissíti a megadott Media Services-fiók elsődleges vagy másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="6328c-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="6328c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6328c-110">EXAMPLES</span></span>

### <span data-ttu-id="6328c-111">1. példa: a Media Services-fiók kulcsának frissítése</span><span class="sxs-lookup"><span data-stu-id="6328c-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="6328c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6328c-112">PARAMETERS</span></span>

### <span data-ttu-id="6328c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6328c-113">-Force</span></span>
<span data-ttu-id="6328c-114">Azt jelzi, hogy a kulcs-generálást nem erősítették meg.</span><span class="sxs-lookup"><span data-stu-id="6328c-114">Indicates that the key generation is not confirmed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6328c-115">-Típus</span><span class="sxs-lookup"><span data-stu-id="6328c-115">-KeyType</span></span>
<span data-ttu-id="6328c-116">A Media Services kulcs típusát adja meg; Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6328c-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="6328c-117">Elsődleges</span><span class="sxs-lookup"><span data-stu-id="6328c-117">Primary</span></span>
- <span data-ttu-id="6328c-118">Másodlagos</span><span class="sxs-lookup"><span data-stu-id="6328c-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6328c-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6328c-119">-Name</span></span>
<span data-ttu-id="6328c-120">A Media Services-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6328c-120">Specifies the name of the Media Services account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6328c-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="6328c-121">-Profile</span></span>
<span data-ttu-id="6328c-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6328c-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6328c-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6328c-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6328c-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6328c-124">-Confirm</span></span>
<span data-ttu-id="6328c-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6328c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6328c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6328c-126">-WhatIf</span></span>
<span data-ttu-id="6328c-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6328c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6328c-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6328c-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6328c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6328c-129">CommonParameters</span></span>
<span data-ttu-id="6328c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6328c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6328c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6328c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6328c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6328c-132">INPUTS</span></span>

## <span data-ttu-id="6328c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6328c-133">OUTPUTS</span></span>

## <span data-ttu-id="6328c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6328c-134">NOTES</span></span>

## <span data-ttu-id="6328c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6328c-135">RELATED LINKS</span></span>

[<span data-ttu-id="6328c-136">Az Azure PowerShell for Media Services használata</span><span class="sxs-lookup"><span data-stu-id="6328c-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)



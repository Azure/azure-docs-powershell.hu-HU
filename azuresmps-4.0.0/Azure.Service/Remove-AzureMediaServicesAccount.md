---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016471"
---
# <span data-ttu-id="b41f2-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b41f2-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="b41f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b41f2-102">SYNOPSIS</span></span>
<span data-ttu-id="b41f2-103">Eltávolítja a megadott Azure Media Services-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b41f2-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="b41f2-104">**Megjegyzés:**  Ez a verzió elavult, kérjük, olvassa el az [újabb verziót](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="b41f2-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="b41f2-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b41f2-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b41f2-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b41f2-106">DESCRIPTION</span></span>
<span data-ttu-id="b41f2-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="b41f2-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b41f2-108">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b41f2-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b41f2-109">A **Remove-AzureMediaServicesAccount** parancsmag eltávolítja a Media Services-fiókot.</span><span class="sxs-lookup"><span data-stu-id="b41f2-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="b41f2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b41f2-110">EXAMPLES</span></span>

### <span data-ttu-id="b41f2-111">1. példa: a Media Services-fiók törlése</span><span class="sxs-lookup"><span data-stu-id="b41f2-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="b41f2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b41f2-112">PARAMETERS</span></span>

### <span data-ttu-id="b41f2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b41f2-113">-Force</span></span>
<span data-ttu-id="b41f2-114">Ha meg van adva az *erő* kapcsoló, a törlés nincs megerősítve.</span><span class="sxs-lookup"><span data-stu-id="b41f2-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="b41f2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b41f2-115">-Name</span></span>
<span data-ttu-id="b41f2-116">A Media Services-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b41f2-116">The Media Services account name.</span></span>

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

### <span data-ttu-id="b41f2-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="b41f2-117">-Profile</span></span>
<span data-ttu-id="b41f2-118">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b41f2-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b41f2-119">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b41f2-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b41f2-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b41f2-120">-Confirm</span></span>
<span data-ttu-id="b41f2-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b41f2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b41f2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b41f2-122">-WhatIf</span></span>
<span data-ttu-id="b41f2-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b41f2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b41f2-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b41f2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b41f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41f2-125">CommonParameters</span></span>
<span data-ttu-id="b41f2-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b41f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41f2-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41f2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41f2-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b41f2-128">INPUTS</span></span>

## <span data-ttu-id="b41f2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b41f2-129">OUTPUTS</span></span>

## <span data-ttu-id="b41f2-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b41f2-130">NOTES</span></span>

## <span data-ttu-id="b41f2-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b41f2-131">RELATED LINKS</span></span>

[<span data-ttu-id="b41f2-132">Az Azure PowerShell for Media Services használata</span><span class="sxs-lookup"><span data-stu-id="b41f2-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="b41f2-133">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b41f2-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="b41f2-134">Új – AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b41f2-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)



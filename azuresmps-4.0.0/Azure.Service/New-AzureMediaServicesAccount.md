---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015911"
---
# <span data-ttu-id="fd803-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd803-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="fd803-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd803-102">SYNOPSIS</span></span>
<span data-ttu-id="fd803-103">Azure Media Services-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fd803-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="fd803-104">**Megjegyzés:** Ez a verzió elavult, kérjük, olvassa el az [újabb verziót](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="fd803-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="fd803-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd803-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fd803-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd803-106">DESCRIPTION</span></span>
<span data-ttu-id="fd803-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="fd803-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fd803-108">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fd803-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fd803-109">A **New-AzureMediaServicesAccount** parancsmag létrehoz egy új Media Services-fiókot, amelyen a megadott Media Services-fiók neve, Datacenter-hely, ahol létre szeretné hozni a fiókot, és egy meglévő tárolási fiók nevét.</span><span class="sxs-lookup"><span data-stu-id="fd803-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="fd803-110">A tárolási fióknak az új Media Services-fiókkal megegyező adatközpontban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fd803-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="fd803-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fd803-111">EXAMPLES</span></span>

### <span data-ttu-id="fd803-112">Példa 1: új Media Services-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="fd803-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="fd803-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd803-113">PARAMETERS</span></span>

### <span data-ttu-id="fd803-114">-Hely</span><span class="sxs-lookup"><span data-stu-id="fd803-114">-Location</span></span>
<span data-ttu-id="fd803-115">A Media Services-adatközpont helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd803-115">Specifies the Media Services datacenter location.</span></span>

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

### <span data-ttu-id="fd803-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fd803-116">-Name</span></span>
<span data-ttu-id="fd803-117">A Media Services-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd803-117">Specifies the Media Services account name.</span></span>

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

### <span data-ttu-id="fd803-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="fd803-118">-Profile</span></span>
<span data-ttu-id="fd803-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="fd803-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fd803-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="fd803-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fd803-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fd803-121">-StorageAccountName</span></span>
<span data-ttu-id="fd803-122">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd803-122">Specifies the storage account name.</span></span>
<span data-ttu-id="fd803-123">A tárterület-fióknak már léteznie kell ugyanabban az adatközpontban, mint az új Media Services-fiók.</span><span class="sxs-lookup"><span data-stu-id="fd803-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

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

### <span data-ttu-id="fd803-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd803-124">CommonParameters</span></span>
<span data-ttu-id="fd803-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd803-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd803-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd803-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd803-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd803-127">INPUTS</span></span>

## <span data-ttu-id="fd803-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd803-128">OUTPUTS</span></span>

## <span data-ttu-id="fd803-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd803-129">NOTES</span></span>

## <span data-ttu-id="fd803-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd803-130">RELATED LINKS</span></span>

[<span data-ttu-id="fd803-131">Az Azure PowerShell for Media Services használata</span><span class="sxs-lookup"><span data-stu-id="fd803-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="fd803-132">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd803-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="fd803-133">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fd803-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)



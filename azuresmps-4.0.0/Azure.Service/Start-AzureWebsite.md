---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015770"
---
# <span data-ttu-id="39ce5-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="39ce5-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="39ce5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="39ce5-103">Elindítja a megadott webhelyet.</span><span class="sxs-lookup"><span data-stu-id="39ce5-103">Starts the specified website.</span></span>

## <span data-ttu-id="39ce5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39ce5-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="39ce5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="39ce5-105">DESCRIPTION</span></span>
<span data-ttu-id="39ce5-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="39ce5-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="39ce5-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="39ce5-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="39ce5-108">A **Start-AzureWebsite** parancsmag az Azure-ban futó meghatározott webhelyt indítja el.</span><span class="sxs-lookup"><span data-stu-id="39ce5-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="39ce5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="39ce5-109">EXAMPLES</span></span>

## <span data-ttu-id="39ce5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39ce5-110">PARAMETERS</span></span>

### <span data-ttu-id="39ce5-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39ce5-111">-Name</span></span>
<span data-ttu-id="39ce5-112">Annak a webhelynek a neve, amelyet meg szeretne kezdeni.</span><span class="sxs-lookup"><span data-stu-id="39ce5-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="39ce5-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39ce5-113">-PassThru</span></span>
<span data-ttu-id="39ce5-114">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="39ce5-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="39ce5-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="39ce5-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="39ce5-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="39ce5-116">-Profile</span></span>
<span data-ttu-id="39ce5-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="39ce5-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="39ce5-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="39ce5-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39ce5-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="39ce5-119">-Slot</span></span>
<span data-ttu-id="39ce5-120">A webhely tárolóhelyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39ce5-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="39ce5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ce5-121">CommonParameters</span></span>
<span data-ttu-id="39ce5-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39ce5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ce5-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ce5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ce5-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39ce5-124">INPUTS</span></span>

## <span data-ttu-id="39ce5-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39ce5-125">OUTPUTS</span></span>

## <span data-ttu-id="39ce5-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39ce5-126">NOTES</span></span>

## <span data-ttu-id="39ce5-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39ce5-127">RELATED LINKS</span></span>

[<span data-ttu-id="39ce5-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="39ce5-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="39ce5-129">Újraindítás – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="39ce5-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="39ce5-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="39ce5-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="39ce5-131">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="39ce5-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="39ce5-132">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="39ce5-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)



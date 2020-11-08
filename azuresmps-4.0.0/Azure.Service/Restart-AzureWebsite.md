---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015470"
---
# <span data-ttu-id="6e136-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6e136-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="6e136-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e136-102">SYNOPSIS</span></span>
<span data-ttu-id="6e136-103">A megadott webhely leállítása és újraindítása.</span><span class="sxs-lookup"><span data-stu-id="6e136-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="6e136-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e136-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e136-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e136-105">DESCRIPTION</span></span>
<span data-ttu-id="6e136-106">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="6e136-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6e136-107">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6e136-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6e136-108">Az **Újraindítás – AzureWebsite** parancsmag leáll, majd újraindítja a megadott webhelyet.</span><span class="sxs-lookup"><span data-stu-id="6e136-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="6e136-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6e136-109">EXAMPLES</span></span>

### <span data-ttu-id="6e136-110">1. példa: webhely újraindítása</span><span class="sxs-lookup"><span data-stu-id="6e136-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="6e136-111">Ez a példa egy MyWebsite nevű webhelyet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6e136-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="6e136-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e136-112">PARAMETERS</span></span>

### <span data-ttu-id="6e136-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e136-113">-Name</span></span>
<span data-ttu-id="6e136-114">Annak az Azure-webhelynek a neve, amelyet újra kell indítani.</span><span class="sxs-lookup"><span data-stu-id="6e136-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="6e136-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e136-115">-PassThru</span></span>
<span data-ttu-id="6e136-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6e136-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6e136-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6e136-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e136-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="6e136-118">-Profile</span></span>
<span data-ttu-id="6e136-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6e136-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e136-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6e136-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e136-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="6e136-121">-Slot</span></span>
<span data-ttu-id="6e136-122">A webhely tárolóhelyének a nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e136-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="6e136-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e136-123">CommonParameters</span></span>
<span data-ttu-id="6e136-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e136-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e136-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e136-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e136-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e136-126">INPUTS</span></span>

## <span data-ttu-id="6e136-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e136-127">OUTPUTS</span></span>

## <span data-ttu-id="6e136-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e136-128">NOTES</span></span>

## <span data-ttu-id="6e136-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e136-129">RELATED LINKS</span></span>

[<span data-ttu-id="6e136-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6e136-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6e136-131">Új – AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6e136-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6e136-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6e136-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="6e136-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6e136-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)



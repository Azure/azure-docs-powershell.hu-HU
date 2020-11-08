---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015819"
---
# <span data-ttu-id="6891e-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6891e-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="6891e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6891e-102">SYNOPSIS</span></span>
<span data-ttu-id="6891e-103">Az aktuális szolgáltatás alapértelmezett helyének, előfizetésének, tárolóhelyének és tárolási fiókjának beállítása.</span><span class="sxs-lookup"><span data-stu-id="6891e-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="6891e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6891e-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6891e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6891e-105">DESCRIPTION</span></span>
<span data-ttu-id="6891e-106">A **set-AzureServiceProject** parancsmag a bevezetési helyet, a bővítőhelyet, a tárolási fiókot és az aktuális szolgáltatás előfizetését állítja be.</span><span class="sxs-lookup"><span data-stu-id="6891e-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="6891e-107">Ezek az értékek akkor használhatók, amikor a szolgáltatást közzéteszi a felhőben.</span><span class="sxs-lookup"><span data-stu-id="6891e-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="6891e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6891e-108">EXAMPLES</span></span>

### <span data-ttu-id="6891e-109">1. példa: alapvető beállítások</span><span class="sxs-lookup"><span data-stu-id="6891e-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="6891e-110">A szolgáltatás üzembe helyezési helyének beállítása az észak-közép-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="6891e-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="6891e-111">Beállítja a telepítő bővítőhelyét a termeléshez.</span><span class="sxs-lookup"><span data-stu-id="6891e-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="6891e-112">Beállítja azt a tárolási fiókot, amely a myStorageAccount a szolgáltatás meghatározásához fog szolgálni.</span><span class="sxs-lookup"><span data-stu-id="6891e-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="6891e-113">Beállítja azt az előfizetést, amely a szolgáltatást a mySubscription-ra fogja üzemeltetni.</span><span class="sxs-lookup"><span data-stu-id="6891e-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="6891e-114">Minden alkalommal, amikor a szolgáltatást közzéteszi a felhőben, az az észak-közép-amerikai régióban található adatközpontban fog megjelenni, és a megadott előfizetési és tárolási fiókot fogja használni.</span><span class="sxs-lookup"><span data-stu-id="6891e-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="6891e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6891e-115">PARAMETERS</span></span>

### <span data-ttu-id="6891e-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="6891e-116">-Location</span></span>
<span data-ttu-id="6891e-117">Az a terület, ahol a szolgáltatást üzemeltetni fogják.</span><span class="sxs-lookup"><span data-stu-id="6891e-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="6891e-118">Ezt az értéket akkor használja a rendszer, amikor a szolgáltatást közzéteszi a felhőben.</span><span class="sxs-lookup"><span data-stu-id="6891e-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="6891e-119">Lehetséges értékek: bárhol Ázsiában, bárhol Európában, bárhol, Kelet-ázsiai, Dél-Közép-amerikai, észak-európai, Dél-Közép-amerikai, Délkelet-ázsiai, Nyugat-európai, Nyugat-amerikai.</span><span class="sxs-lookup"><span data-stu-id="6891e-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

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

### <span data-ttu-id="6891e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6891e-120">-PassThru</span></span>
<span data-ttu-id="6891e-121">Azt jelzi, hogy ez a parancsmag egy olyan objektumot ad eredményül, amely a működéséhez szükséges elemet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6891e-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="6891e-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6891e-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6891e-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="6891e-123">-Profile</span></span>
<span data-ttu-id="6891e-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="6891e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6891e-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="6891e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6891e-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="6891e-126">-Slot</span></span>
<span data-ttu-id="6891e-127">Az a tárolóhely (termelés vagy megállóhely), amelyben a szolgáltatást üzemeltetni fogják.</span><span class="sxs-lookup"><span data-stu-id="6891e-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="6891e-128">Ezt az értéket akkor használja a rendszer, amikor a szolgáltatást közzéteszi a felhőben.</span><span class="sxs-lookup"><span data-stu-id="6891e-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="6891e-129">Lehetséges értékek: termelés, megállóhelyek.</span><span class="sxs-lookup"><span data-stu-id="6891e-129">Possible values are: Production, Staging.</span></span>

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

### <span data-ttu-id="6891e-130">-Tárterület</span><span class="sxs-lookup"><span data-stu-id="6891e-130">-Storage</span></span>
<span data-ttu-id="6891e-131">A szervizcsomagnak a felhőbe való feltöltéséhez használandó tárolási fiók.</span><span class="sxs-lookup"><span data-stu-id="6891e-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="6891e-132">Ha a tárolási fiók nem létezik, akkor a rendszer akkor hozza létre, amikor a szolgáltatást közzéteszi a felhőben.</span><span class="sxs-lookup"><span data-stu-id="6891e-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

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

### <span data-ttu-id="6891e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6891e-133">CommonParameters</span></span>
<span data-ttu-id="6891e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6891e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6891e-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6891e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6891e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6891e-136">INPUTS</span></span>

## <span data-ttu-id="6891e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6891e-137">OUTPUTS</span></span>

## <span data-ttu-id="6891e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6891e-138">NOTES</span></span>
* <span data-ttu-id="6891e-139">Node-dev, php-dev, Python-dev</span><span class="sxs-lookup"><span data-stu-id="6891e-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="6891e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6891e-140">RELATED LINKS</span></span>

[<span data-ttu-id="6891e-141">Új – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6891e-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="6891e-142">Közzététel – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6891e-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="6891e-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="6891e-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)



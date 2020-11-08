---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015993"
---
# <span data-ttu-id="c658b-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="c658b-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="c658b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c658b-102">SYNOPSIS</span></span>
<span data-ttu-id="c658b-103">Fenntartott IP-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c658b-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="c658b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c658b-104">SYNTAX</span></span>

### <span data-ttu-id="c658b-105">CreateNewReservedIP (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c658b-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c658b-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="c658b-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c658b-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="c658b-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c658b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c658b-108">DESCRIPTION</span></span>
<span data-ttu-id="c658b-109">A **New-AzureReservedIP** parancsmag létrehoz egy FENNTARTott IP-címet.</span><span class="sxs-lookup"><span data-stu-id="c658b-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="c658b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c658b-110">EXAMPLES</span></span>

### <span data-ttu-id="c658b-111">1. példa: új fenntartott IP-cím létrehozása</span><span class="sxs-lookup"><span data-stu-id="c658b-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="c658b-112">A parancs létrehoz egy új fenntartott IP-címet az előfizetésben, amely a webes, a munkás és a virtuális gépeket tartalmazó felhőalapú szolgáltatások létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="c658b-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="c658b-113">2. példa: fenntartott IP-cím létrehozása meglévő IP-címen alapul</span><span class="sxs-lookup"><span data-stu-id="c658b-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="c658b-114">Ez a parancs létrehoz egy meglévő VIP-(virtuális IP-címet) a megadott szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c658b-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="c658b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c658b-115">PARAMETERS</span></span>

### <span data-ttu-id="c658b-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c658b-116">-InformationAction</span></span>
<span data-ttu-id="c658b-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="c658b-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c658b-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c658b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c658b-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="c658b-119">Continue</span></span>
- <span data-ttu-id="c658b-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="c658b-120">Ignore</span></span>
- <span data-ttu-id="c658b-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="c658b-121">Inquire</span></span>
- <span data-ttu-id="c658b-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c658b-122">SilentlyContinue</span></span>
- <span data-ttu-id="c658b-123">állj</span><span class="sxs-lookup"><span data-stu-id="c658b-123">Stop</span></span>
- <span data-ttu-id="c658b-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="c658b-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c658b-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c658b-125">-InformationVariable</span></span>
<span data-ttu-id="c658b-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="c658b-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c658b-127">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="c658b-127">-Label</span></span>
<span data-ttu-id="c658b-128">A lefoglalt IP-cím címkéjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c658b-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c658b-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="c658b-129">-Location</span></span>
<span data-ttu-id="c658b-130">Itt adhatja meg azt a helyet, ahol a fenntartott IP-címet létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="c658b-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c658b-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="c658b-131">-Profile</span></span>
<span data-ttu-id="c658b-132">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c658b-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c658b-133">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c658b-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c658b-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="c658b-134">-ReservedIPName</span></span>
<span data-ttu-id="c658b-135">A fenntartott IP-cím nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c658b-135">Specifies the reserved IP address name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c658b-136">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="c658b-136">-ServiceName</span></span>
<span data-ttu-id="c658b-137">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c658b-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c658b-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="c658b-138">-Slot</span></span>
<span data-ttu-id="c658b-139">A telepítő bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c658b-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="c658b-140">A paraméter elfogadható értékei a következők: megállóhelyek, termelés.</span><span class="sxs-lookup"><span data-stu-id="c658b-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c658b-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="c658b-141">-VirtualIPName</span></span>
<span data-ttu-id="c658b-142">Itt adhatja meg, hogy a parancsmag a **VirtualIPName** paraméterrel egy meglévő virtuális IP-címet (VIP) foglaljon le a bevezetésben.</span><span class="sxs-lookup"><span data-stu-id="c658b-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="c658b-143">Ha a paraméter nincs megadva, ez a parancsmag új VIP-t is fenntart.</span><span class="sxs-lookup"><span data-stu-id="c658b-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c658b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c658b-144">CommonParameters</span></span>
<span data-ttu-id="c658b-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c658b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c658b-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c658b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c658b-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c658b-147">INPUTS</span></span>

## <span data-ttu-id="c658b-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c658b-148">OUTPUTS</span></span>

## <span data-ttu-id="c658b-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c658b-149">NOTES</span></span>

## <span data-ttu-id="c658b-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c658b-150">RELATED LINKS</span></span>

[<span data-ttu-id="c658b-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="c658b-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="c658b-152">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="c658b-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)



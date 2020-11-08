---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015825"
---
# <span data-ttu-id="933e4-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="933e4-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="933e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="933e4-102">SYNOPSIS</span></span>
<span data-ttu-id="933e4-103">Fenntartott IP-címet társít egy meglévő virtuális géphez vagy felhőalapú szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="933e4-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="933e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="933e4-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="933e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="933e4-105">DESCRIPTION</span></span>
<span data-ttu-id="933e4-106">A **set-AzureReservedIPAssociation** parancsmag FENNTARTott IP-címet társít egy futó virtuális gép vagy felhőalapú szolgáltatás virtuális IP-címével (VIP).</span><span class="sxs-lookup"><span data-stu-id="933e4-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="933e4-107">A fenntartott IP-cím nem használható az e parancsmag használatakor, és ugyanazon a helyen kell lennie, mint a virtuális gépet vagy a Felhőbeli szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="933e4-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="933e4-108">A művelet körülbelül 30 másodperc elteltével lép életbe, ami után a virtuális gép vagy szolgáltatás elérhető a lefoglalt IP-cím használatával.</span><span class="sxs-lookup"><span data-stu-id="933e4-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="933e4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="933e4-109">EXAMPLES</span></span>

### <span data-ttu-id="933e4-110">1. példa: fenntartott IP-társítás beállítása</span><span class="sxs-lookup"><span data-stu-id="933e4-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="933e4-111">Ez a parancs hozzárendeli a ResIp14 nevű fenntartott IP-címet a szolgáltatás PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="933e4-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="933e4-112">A ResIp14 egy fenntartott IP a Nyugat-európai régióban.</span><span class="sxs-lookup"><span data-stu-id="933e4-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="933e4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="933e4-113">PARAMETERS</span></span>

### <span data-ttu-id="933e4-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="933e4-114">-InformationAction</span></span>
<span data-ttu-id="933e4-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="933e4-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="933e4-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="933e4-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="933e4-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="933e4-117">Continue</span></span>
- <span data-ttu-id="933e4-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="933e4-118">Ignore</span></span>
- <span data-ttu-id="933e4-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="933e4-119">Inquire</span></span>
- <span data-ttu-id="933e4-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="933e4-120">SilentlyContinue</span></span>
- <span data-ttu-id="933e4-121">állj</span><span class="sxs-lookup"><span data-stu-id="933e4-121">Stop</span></span>
- <span data-ttu-id="933e4-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="933e4-122">Suspend</span></span>

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

### <span data-ttu-id="933e4-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="933e4-123">-InformationVariable</span></span>
<span data-ttu-id="933e4-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="933e4-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="933e4-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="933e4-125">-Profile</span></span>
<span data-ttu-id="933e4-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="933e4-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="933e4-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="933e4-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="933e4-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="933e4-128">-ReservedIPName</span></span>
<span data-ttu-id="933e4-129">Annak a fenntartott IP-címnek a nevét adja meg, amelyet egy virtuális géphez vagy szolgáltatáshoz szeretne társítani.</span><span class="sxs-lookup"><span data-stu-id="933e4-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

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

### <span data-ttu-id="933e4-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="933e4-130">-ServiceName</span></span>
<span data-ttu-id="933e4-131">Annak a szolgáltatásnak a nevét adja meg, amelybe a lefoglalt IP-címet társítani szeretné.</span><span class="sxs-lookup"><span data-stu-id="933e4-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933e4-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="933e4-132">-Slot</span></span>
<span data-ttu-id="933e4-133">A telepítő bővítőhelyet adja meg.</span><span class="sxs-lookup"><span data-stu-id="933e4-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="933e4-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="933e4-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="933e4-135">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="933e4-135">Staging</span></span>
- <span data-ttu-id="933e4-136">Production</span><span class="sxs-lookup"><span data-stu-id="933e4-136">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933e4-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="933e4-137">-VirtualIPName</span></span>
<span data-ttu-id="933e4-138">Annak a meglévő VIP-névnek a nevét adja meg, amely társítva van egy fenntartott IP-vel.</span><span class="sxs-lookup"><span data-stu-id="933e4-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="933e4-139">Lásd: Add-AzureVirtualIP a VIP-szolgáltatások hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="933e4-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="933e4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="933e4-140">CommonParameters</span></span>
<span data-ttu-id="933e4-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="933e4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="933e4-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="933e4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="933e4-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="933e4-143">INPUTS</span></span>

## <span data-ttu-id="933e4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="933e4-144">OUTPUTS</span></span>

### <span data-ttu-id="933e4-145">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="933e4-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="933e4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="933e4-146">NOTES</span></span>

## <span data-ttu-id="933e4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="933e4-147">RELATED LINKS</span></span>

[<span data-ttu-id="933e4-148">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="933e4-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)



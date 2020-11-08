---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016136"
---
# <span data-ttu-id="1006b-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="1006b-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="1006b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1006b-102">SYNOPSIS</span></span>
<span data-ttu-id="1006b-103">Eltávolítja a társítást a fenntartott IP-címről a VM vagy a felhő szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="1006b-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="1006b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1006b-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1006b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1006b-105">DESCRIPTION</span></span>
<span data-ttu-id="1006b-106">A **Remove-AzureReservedIPAssociation** parancsmag nem társítja a lefoglalt IP-címet egy virtuális GÉPRŐL (VM) vagy Felhőbeli szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="1006b-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="1006b-107">Amikor a művelet befejeződött, a lefoglalt IP-cím ingyenes, és a VM/VIP megkapja a dinamikus nyilvános IP-címet az Azure Inventory rendszerből.</span><span class="sxs-lookup"><span data-stu-id="1006b-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="1006b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1006b-108">EXAMPLES</span></span>

### <span data-ttu-id="1006b-109">1. példa: fenntartott IP-társítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1006b-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="1006b-110">Ez a parancs nem társítja a ResIp14 nevű fenntartott IP-címet a PipTestWestEurope nevű szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="1006b-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="1006b-111">A PipTestWestEurope egy új dinamikus VIP-felhasználó lesz társítva.</span><span class="sxs-lookup"><span data-stu-id="1006b-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="1006b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1006b-112">PARAMETERS</span></span>

### <span data-ttu-id="1006b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1006b-113">-Force</span></span>
<span data-ttu-id="1006b-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1006b-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="1006b-115">Ezzel a jelzéssel figyelmen kívül hagyhatja az e-maileket a fenntartott IP-társítás eltávolításakor.</span><span class="sxs-lookup"><span data-stu-id="1006b-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1006b-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1006b-116">-InformationAction</span></span>
<span data-ttu-id="1006b-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="1006b-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1006b-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1006b-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1006b-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="1006b-119">Continue</span></span>
- <span data-ttu-id="1006b-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="1006b-120">Ignore</span></span>
- <span data-ttu-id="1006b-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="1006b-121">Inquire</span></span>
- <span data-ttu-id="1006b-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1006b-122">SilentlyContinue</span></span>
- <span data-ttu-id="1006b-123">állj</span><span class="sxs-lookup"><span data-stu-id="1006b-123">Stop</span></span>
- <span data-ttu-id="1006b-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="1006b-124">Suspend</span></span>

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

### <span data-ttu-id="1006b-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1006b-125">-InformationVariable</span></span>
<span data-ttu-id="1006b-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="1006b-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1006b-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="1006b-127">-Profile</span></span>
<span data-ttu-id="1006b-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1006b-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1006b-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1006b-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1006b-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="1006b-130">-ReservedIPName</span></span>
<span data-ttu-id="1006b-131">A foglalt IP-cím nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1006b-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="1006b-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="1006b-132">-ServiceName</span></span>
<span data-ttu-id="1006b-133">A szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1006b-133">Specifies the  name of the service.</span></span>

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

### <span data-ttu-id="1006b-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="1006b-134">-Slot</span></span>
<span data-ttu-id="1006b-135">A központi telepítő környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1006b-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="1006b-136">A paraméter elfogadható értékei a következők: termelés, megállóhelyek.</span><span class="sxs-lookup"><span data-stu-id="1006b-136">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="1006b-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="1006b-137">-VirtualIPName</span></span>
<span data-ttu-id="1006b-138">Azt a virtuális IP-címet adja meg, amelyből el szeretné távolítani a társítást egy szolgáltatással vagy VM-tel.</span><span class="sxs-lookup"><span data-stu-id="1006b-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

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

### <span data-ttu-id="1006b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1006b-139">CommonParameters</span></span>
<span data-ttu-id="1006b-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1006b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1006b-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1006b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1006b-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1006b-142">INPUTS</span></span>

## <span data-ttu-id="1006b-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1006b-143">OUTPUTS</span></span>

### <span data-ttu-id="1006b-144">Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="1006b-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="1006b-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1006b-145">NOTES</span></span>

## <span data-ttu-id="1006b-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1006b-146">RELATED LINKS</span></span>

[<span data-ttu-id="1006b-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="1006b-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)



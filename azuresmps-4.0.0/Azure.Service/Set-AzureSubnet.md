---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015951"
---
# <span data-ttu-id="64209-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="64209-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="64209-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64209-102">SYNOPSIS</span></span>
<span data-ttu-id="64209-103">Egy Azure virtuális gép alhálózatának listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="64209-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="64209-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64209-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="64209-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="64209-105">DESCRIPTION</span></span>
<span data-ttu-id="64209-106">A **set-AzureSubnet** parancsmag a virtuális gép konfigurációjának alhálózati listáját állítja be.</span><span class="sxs-lookup"><span data-stu-id="64209-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="64209-107">Használja a **New-AzureVM** a virtuális gép alhálózatának beállításához.</span><span class="sxs-lookup"><span data-stu-id="64209-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="64209-108">Példák</span><span class="sxs-lookup"><span data-stu-id="64209-108">EXAMPLES</span></span>

### <span data-ttu-id="64209-109">1. példa: alhálózat felvétele virtuális gép konfigurációba</span><span class="sxs-lookup"><span data-stu-id="64209-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="64209-110">A parancs hozzáadja az alhálózatot a virtuálisgép-konfigurációhoz, majd létrehozza a VirtualMachine04 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="64209-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="64209-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64209-111">PARAMETERS</span></span>

### <span data-ttu-id="64209-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="64209-112">-InformationAction</span></span>
<span data-ttu-id="64209-113">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="64209-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="64209-114">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="64209-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64209-115">Folytassa</span><span class="sxs-lookup"><span data-stu-id="64209-115">Continue</span></span>
- <span data-ttu-id="64209-116">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="64209-116">Ignore</span></span>
- <span data-ttu-id="64209-117">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="64209-117">Inquire</span></span>
- <span data-ttu-id="64209-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="64209-118">SilentlyContinue</span></span>
- <span data-ttu-id="64209-119">állj</span><span class="sxs-lookup"><span data-stu-id="64209-119">Stop</span></span>
- <span data-ttu-id="64209-120">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="64209-120">Suspend</span></span>

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

### <span data-ttu-id="64209-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="64209-121">-InformationVariable</span></span>
<span data-ttu-id="64209-122">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="64209-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="64209-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="64209-123">-Profile</span></span>
<span data-ttu-id="64209-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="64209-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64209-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="64209-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64209-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="64209-126">-SubnetNames</span></span>
<span data-ttu-id="64209-127">Az alhálózati nevek listáját tartalmazó tömböt ad meg.</span><span class="sxs-lookup"><span data-stu-id="64209-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64209-128">-VM</span><span class="sxs-lookup"><span data-stu-id="64209-128">-VM</span></span>
<span data-ttu-id="64209-129">A virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="64209-129">Specifies the virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64209-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64209-130">CommonParameters</span></span>
<span data-ttu-id="64209-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64209-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64209-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64209-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64209-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64209-133">INPUTS</span></span>

## <span data-ttu-id="64209-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64209-134">OUTPUTS</span></span>

## <span data-ttu-id="64209-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64209-135">NOTES</span></span>

## <span data-ttu-id="64209-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64209-136">RELATED LINKS</span></span>

[<span data-ttu-id="64209-137">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="64209-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="64209-138">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="64209-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="64209-139">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="64209-139">Update-AzureVM</span></span>](./Update-AzureVM.md)



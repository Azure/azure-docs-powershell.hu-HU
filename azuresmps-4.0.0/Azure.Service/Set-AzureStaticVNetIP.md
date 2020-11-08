---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015862"
---
# <span data-ttu-id="b5f3a-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="b5f3a-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="b5f3a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f3a-103">A virtuális gép objektum statikus VNet IP-címének adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="b5f3a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5f3a-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5f3a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f3a-106">A **set-AzureStaticVNetIP** parancsmag a virtuális gép objektum statikus virtuális hálózat (VNet) IP-címének adatait állítja be.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="b5f3a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b5f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="b5f3a-108">Példa 1: a virtuális géphez társított virtuális hálózat IP-címének beállítása</span><span class="sxs-lookup"><span data-stu-id="b5f3a-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="b5f3a-109">Az első parancs beállítja a virtuális hálózat konfigurációs elérési útját.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="b5f3a-110">A második parancs a virtuálisgép-konfigurációt hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="b5f3a-111">A harmadik parancs a virtuális gép alhálózatát állítja be.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="b5f3a-112">A negyedik parancs beállítja a virtuális gép IP-címét.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="b5f3a-113">Az ötödik parancs virtuális gépet hoz létre a virtuális gép segítségével.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="b5f3a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5f3a-114">PARAMETERS</span></span>

### <span data-ttu-id="b5f3a-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b5f3a-115">-InformationAction</span></span>
<span data-ttu-id="b5f3a-116">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5f3a-117">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b5f3a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5f3a-118">Folytassa</span><span class="sxs-lookup"><span data-stu-id="b5f3a-118">Continue</span></span>
- <span data-ttu-id="b5f3a-119">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="b5f3a-119">Ignore</span></span>
- <span data-ttu-id="b5f3a-120">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="b5f3a-120">Inquire</span></span>
- <span data-ttu-id="b5f3a-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5f3a-121">SilentlyContinue</span></span>
- <span data-ttu-id="b5f3a-122">állj</span><span class="sxs-lookup"><span data-stu-id="b5f3a-122">Stop</span></span>
- <span data-ttu-id="b5f3a-123">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="b5f3a-123">Suspend</span></span>

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

### <span data-ttu-id="b5f3a-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5f3a-124">-InformationVariable</span></span>
<span data-ttu-id="b5f3a-125">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5f3a-126">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="b5f3a-126">-IPAddress</span></span>
<span data-ttu-id="b5f3a-127">A statikus VNet IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3a-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="b5f3a-128">-Profile</span></span>
<span data-ttu-id="b5f3a-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5f3a-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5f3a-131">-VM</span><span class="sxs-lookup"><span data-stu-id="b5f3a-131">-VM</span></span>
<span data-ttu-id="b5f3a-132">Olyan állandó virtuálisgép-objektumot ad meg, amelyhez a statikus VNet IP-címét be szeretné állítani.</span><span class="sxs-lookup"><span data-stu-id="b5f3a-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="b5f3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f3a-133">CommonParameters</span></span>
<span data-ttu-id="b5f3a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5f3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f3a-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f3a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f3a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5f3a-136">INPUTS</span></span>

## <span data-ttu-id="b5f3a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5f3a-137">OUTPUTS</span></span>

## <span data-ttu-id="b5f3a-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5f3a-138">NOTES</span></span>

## <span data-ttu-id="b5f3a-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5f3a-139">RELATED LINKS</span></span>

[<span data-ttu-id="b5f3a-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="b5f3a-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="b5f3a-141">Teszt-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="b5f3a-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)



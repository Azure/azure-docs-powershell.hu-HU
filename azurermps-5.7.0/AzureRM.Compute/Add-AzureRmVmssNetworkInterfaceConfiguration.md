---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672037"
---
# <span data-ttu-id="ca9c4-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca9c4-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="ca9c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9c4-103">Hálózati illesztőfelület-konfiguráció felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca9c4-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca9c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca9c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9c4-106">Az **Add-AzureRmVmssNetworkInterfaceConfiguration** parancsmag hálózati illesztőfelület-konfigurációt ad hozzá a Virtual Machine Scale set (VMSS) beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ca9c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca9c4-107">EXAMPLES</span></span>

### <span data-ttu-id="ca9c4-108">Példa 1: hálózati illesztőfelület-konfiguráció felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="ca9c4-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="ca9c4-109">Ez a parancs hálózati illesztőfelület-konfigurációt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="ca9c4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca9c4-110">PARAMETERS</span></span>

### <span data-ttu-id="ca9c4-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="ca9c4-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="ca9c4-112">A DNS-kiszolgálók IP-címeinek listája a DNS-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c4-113">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ca9c4-113">-Id</span></span>
<span data-ttu-id="ca9c4-114">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-114">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="ca9c4-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ca9c4-115">-IpConfiguration</span></span>
<span data-ttu-id="ca9c4-116">A hálózati felület IP-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-116">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca9c4-117">-Name</span></span>
<span data-ttu-id="ca9c4-118">A hálózati felület konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-118">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="ca9c4-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ca9c4-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="ca9c4-120">A hálózati biztonsági csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="ca9c4-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="ca9c4-121">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="ca9c4-121">-Primary</span></span>
<span data-ttu-id="ca9c4-122">Azt jelzi, hogy a hálózati illesztőfelület-konfigurációból létrehozott hálózati felületek a virtuális gép elsődleges hálózati információs központja (NIC) fogják-e létrehozni.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c4-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ca9c4-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ca9c4-124">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="ca9c4-125">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c4-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca9c4-126">-Confirm</span></span>
<span data-ttu-id="ca9c4-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca9c4-128">-WhatIf</span></span>
<span data-ttu-id="ca9c4-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca9c4-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9c4-131">CommonParameters</span></span>
<span data-ttu-id="ca9c4-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca9c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9c4-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9c4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9c4-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca9c4-134">INPUTS</span></span>

### <span data-ttu-id="ca9c4-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="ca9c4-135">None</span></span>
<span data-ttu-id="ca9c4-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ca9c4-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca9c4-137">OUTPUTS</span></span>

###  
<span data-ttu-id="ca9c4-138">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ca9c4-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ca9c4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca9c4-139">NOTES</span></span>

## <span data-ttu-id="ca9c4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca9c4-140">RELATED LINKS</span></span>

[<span data-ttu-id="ca9c4-141">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ca9c4-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

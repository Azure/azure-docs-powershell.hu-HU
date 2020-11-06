---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499196"
---
# <span data-ttu-id="d678e-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d678e-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="d678e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d678e-102">SYNOPSIS</span></span>
<span data-ttu-id="d678e-103">Hálózati illesztőfelület-konfiguráció felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="d678e-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d678e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d678e-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d678e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d678e-105">DESCRIPTION</span></span>
<span data-ttu-id="d678e-106">Az **Add-AzureRmVmssNetworkInterfaceConfiguration** parancsmag hálózati illesztőfelület-konfigurációt ad hozzá a Virtual Machine Scale set (VMSS) beállításhoz.</span><span class="sxs-lookup"><span data-stu-id="d678e-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d678e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d678e-107">EXAMPLES</span></span>

### <span data-ttu-id="d678e-108">Példa 1: hálózati illesztőfelület-konfiguráció felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="d678e-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="d678e-109">Ez a parancs hálózati illesztőfelület-konfigurációt ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="d678e-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="d678e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d678e-110">PARAMETERS</span></span>

### <span data-ttu-id="d678e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d678e-111">-DefaultProfile</span></span>
<span data-ttu-id="d678e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d678e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="d678e-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="d678e-114">A DNS-kiszolgálók IP-címeinek listája a DNS-beállításokhoz.</span><span class="sxs-lookup"><span data-stu-id="d678e-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="d678e-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="d678e-116">Azt adja meg, hogy a hálózati felület gyorsított hálózati kapcsolaton van-e.</span><span class="sxs-lookup"><span data-stu-id="d678e-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d678e-117">-Id</span></span>
<span data-ttu-id="d678e-118">A virtuális gép erőforrás-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d678e-118">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d678e-119">-IpConfiguration</span></span>
<span data-ttu-id="d678e-120">A hálózati felület IP-konfigurációit adja meg.</span><span class="sxs-lookup"><span data-stu-id="d678e-120">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d678e-121">-Name</span></span>
<span data-ttu-id="d678e-122">A hálózati felület konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d678e-122">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d678e-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d678e-124">A hálózati biztonsági csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="d678e-124">Id of the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-125">-Elsődleges</span><span class="sxs-lookup"><span data-stu-id="d678e-125">-Primary</span></span>
<span data-ttu-id="d678e-126">Azt jelzi, hogy a hálózati illesztőfelület-konfigurációból létrehozott hálózati felületek a virtuális gép elsődleges hálózati információs központja (NIC) fogják-e létrehozni.</span><span class="sxs-lookup"><span data-stu-id="d678e-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d678e-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d678e-128">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d678e-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="d678e-129">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d678e-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d678e-130">-Confirm</span></span>
<span data-ttu-id="d678e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d678e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d678e-132">-WhatIf</span></span>
<span data-ttu-id="d678e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d678e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d678e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d678e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d678e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d678e-135">CommonParameters</span></span>
<span data-ttu-id="d678e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d678e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d678e-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d678e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d678e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d678e-138">INPUTS</span></span>

## <span data-ttu-id="d678e-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d678e-139">OUTPUTS</span></span>

###  
<span data-ttu-id="d678e-140">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d678e-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d678e-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d678e-141">NOTES</span></span>

## <span data-ttu-id="d678e-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d678e-142">RELATED LINKS</span></span>

[<span data-ttu-id="d678e-143">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d678e-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

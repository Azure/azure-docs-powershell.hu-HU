---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024165"
---
# <span data-ttu-id="562c8-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="562c8-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="562c8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="562c8-102">SYNOPSIS</span></span>
<span data-ttu-id="562c8-103">Hozzáadja a WinRM-figyelőt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="562c8-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="562c8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="562c8-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="562c8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="562c8-105">DESCRIPTION</span></span>
<span data-ttu-id="562c8-106">A **Add-AzVmssWinRMListener** parancsmag a Windows távfelügyelet (WinRM) bővítményét a Virtual Machine Scale set (VMSS) rendszerhez adja.</span><span class="sxs-lookup"><span data-stu-id="562c8-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="562c8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="562c8-107">EXAMPLES</span></span>

### <span data-ttu-id="562c8-108">1. példa: a WinRM-figyelő felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="562c8-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="562c8-109">Ez a példa a WinRM-figyelőt felveszi a VMSS.</span><span class="sxs-lookup"><span data-stu-id="562c8-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="562c8-110">Az első parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="562c8-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="562c8-111">A második parancs hozzáadja a HTTP Protocol WinRM-figyelőt a megadott URL-címen található VMSS.</span><span class="sxs-lookup"><span data-stu-id="562c8-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="562c8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="562c8-112">PARAMETERS</span></span>

### <span data-ttu-id="562c8-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="562c8-113">-CertificateUrl</span></span>
<span data-ttu-id="562c8-114">Annak a tanúsítványnak a hivatkozását adja meg URL-címként, amelyen az új virtuális gépek kiépítése megtörténik.</span><span class="sxs-lookup"><span data-stu-id="562c8-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="562c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="562c8-115">-DefaultProfile</span></span>
<span data-ttu-id="562c8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="562c8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="562c8-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="562c8-117">-Protocol</span></span>
<span data-ttu-id="562c8-118">A WinRM-figyelő protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="562c8-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="562c8-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="562c8-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="562c8-120">Http</span><span class="sxs-lookup"><span data-stu-id="562c8-120">Http</span></span>
- <span data-ttu-id="562c8-121">Https</span><span class="sxs-lookup"><span data-stu-id="562c8-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="562c8-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="562c8-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="562c8-123">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="562c8-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="562c8-124">Az objektum létrehozásához az New-AzVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="562c8-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="562c8-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="562c8-125">-Confirm</span></span>
<span data-ttu-id="562c8-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="562c8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="562c8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="562c8-127">-WhatIf</span></span>
<span data-ttu-id="562c8-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="562c8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="562c8-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="562c8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="562c8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="562c8-130">CommonParameters</span></span>
<span data-ttu-id="562c8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="562c8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="562c8-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="562c8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="562c8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="562c8-133">INPUTS</span></span>

### <span data-ttu-id="562c8-134">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="562c8-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="562c8-135">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. ProtocolTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="562c8-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="562c8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="562c8-136">System.String</span></span>

## <span data-ttu-id="562c8-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="562c8-137">OUTPUTS</span></span>

### <span data-ttu-id="562c8-138">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="562c8-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="562c8-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="562c8-139">NOTES</span></span>

## <span data-ttu-id="562c8-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="562c8-140">RELATED LINKS</span></span>

[<span data-ttu-id="562c8-141">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="562c8-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)



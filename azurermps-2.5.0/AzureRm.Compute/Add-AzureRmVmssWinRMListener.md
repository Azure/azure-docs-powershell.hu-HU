---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsswinrmlistener
schema: 2.0.0
ms.openlocfilehash: dd9c13298adac34a53ed2f97bbc1e3edc95892df
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848933"
---
# <span data-ttu-id="f1268-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="f1268-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="f1268-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1268-102">SYNOPSIS</span></span>
<span data-ttu-id="f1268-103">Hozzáadja a WinRM-figyelőt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1268-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1268-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1268-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1268-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1268-105">DESCRIPTION</span></span>
<span data-ttu-id="f1268-106">A **Add-AzureRmVmssWinRMListener** parancsmag a Windows távfelügyelet (WinRM) bővítményét a Virtual Machine Scale set (VMSS) rendszerhez adja.</span><span class="sxs-lookup"><span data-stu-id="f1268-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f1268-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1268-107">EXAMPLES</span></span>

### <span data-ttu-id="f1268-108">1. példa: a WinRM-figyelő felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="f1268-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="f1268-109">Ez a példa a WinRM-figyelőt felveszi a VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1268-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="f1268-110">Az első parancs a **New-AzureRmVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f1268-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="f1268-111">A második parancs hozzáadja a HTTP Protocol WinRM-figyelőt a megadott URL-címen található VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1268-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="f1268-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1268-112">PARAMETERS</span></span>

### <span data-ttu-id="f1268-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="f1268-113">-CertificateUrl</span></span>
<span data-ttu-id="f1268-114">Annak a tanúsítványnak a hivatkozását adja meg URL-címként, amelyen az új virtuális gépek kiépítése megtörténik.</span><span class="sxs-lookup"><span data-stu-id="f1268-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="f1268-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1268-115">-DefaultProfile</span></span>
<span data-ttu-id="f1268-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1268-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1268-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f1268-117">-Protocol</span></span>
<span data-ttu-id="f1268-118">A WinRM-figyelő protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1268-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="f1268-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f1268-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1268-120">Http</span><span class="sxs-lookup"><span data-stu-id="f1268-120">Http</span></span>
- <span data-ttu-id="f1268-121">Https</span><span class="sxs-lookup"><span data-stu-id="f1268-121">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1268-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f1268-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f1268-123">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1268-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="f1268-124">Az objektum létrehozásához az New-AzureRmVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="f1268-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1268-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1268-125">-Confirm</span></span>
<span data-ttu-id="f1268-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1268-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1268-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1268-127">-WhatIf</span></span>
<span data-ttu-id="f1268-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1268-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1268-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1268-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1268-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1268-130">CommonParameters</span></span>
<span data-ttu-id="f1268-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1268-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1268-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1268-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1268-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1268-133">INPUTS</span></span>

### <span data-ttu-id="f1268-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f1268-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="f1268-135">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f1268-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="f1268-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1268-136">OUTPUTS</span></span>

### <span data-ttu-id="f1268-137">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f1268-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f1268-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1268-138">NOTES</span></span>

## <span data-ttu-id="f1268-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1268-139">RELATED LINKS</span></span>

[<span data-ttu-id="f1268-140">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f1268-140">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)



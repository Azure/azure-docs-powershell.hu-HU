---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 00e61142948e42310dbd5c0be56660c17ec7e8e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844702"
---
# <span data-ttu-id="6fe9c-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="6fe9c-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="6fe9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fe9c-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe9c-103">Hozzáadja a WinRM-figyelőt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="6fe9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fe9c-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fe9c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fe9c-105">DESCRIPTION</span></span>
<span data-ttu-id="6fe9c-106">A **Add-AzVmssWinRMListener** parancsmag a Windows távfelügyelet (WinRM) bővítményét a Virtual Machine Scale set (VMSS) rendszerhez adja.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="6fe9c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6fe9c-107">EXAMPLES</span></span>

### <span data-ttu-id="6fe9c-108">1. példa: a WinRM-figyelő felvétele a VMSS</span><span class="sxs-lookup"><span data-stu-id="6fe9c-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="6fe9c-109">Ez a példa a WinRM-figyelőt felveszi a VMSS.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="6fe9c-110">Az első parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="6fe9c-111">A második parancs hozzáadja a HTTP Protocol WinRM-figyelőt a megadott URL-címen található VMSS.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="6fe9c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fe9c-112">PARAMETERS</span></span>

### <span data-ttu-id="6fe9c-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="6fe9c-113">-CertificateUrl</span></span>
<span data-ttu-id="6fe9c-114">Annak a tanúsítványnak a hivatkozását adja meg URL-címként, amelyen az új virtuális gépek kiépítése megtörténik.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="6fe9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe9c-115">-DefaultProfile</span></span>
<span data-ttu-id="6fe9c-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fe9c-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6fe9c-117">-Protocol</span></span>
<span data-ttu-id="6fe9c-118">A WinRM-figyelő protokollját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="6fe9c-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6fe9c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6fe9c-120">Http</span><span class="sxs-lookup"><span data-stu-id="6fe9c-120">Http</span></span>
- <span data-ttu-id="6fe9c-121">Https</span><span class="sxs-lookup"><span data-stu-id="6fe9c-121">Https</span></span>

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

### <span data-ttu-id="6fe9c-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6fe9c-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6fe9c-123">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="6fe9c-124">Az objektum létrehozásához az New-AzVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="6fe9c-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6fe9c-125">-Confirm</span></span>
<span data-ttu-id="6fe9c-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe9c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe9c-127">-WhatIf</span></span>
<span data-ttu-id="6fe9c-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fe9c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe9c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe9c-130">CommonParameters</span></span>
<span data-ttu-id="6fe9c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fe9c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe9c-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe9c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe9c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe9c-133">INPUTS</span></span>

### <span data-ttu-id="6fe9c-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6fe9c-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="6fe9c-135">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6fe9c-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="6fe9c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe9c-136">OUTPUTS</span></span>

### <span data-ttu-id="6fe9c-137">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6fe9c-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6fe9c-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fe9c-138">NOTES</span></span>

## <span data-ttu-id="6fe9c-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fe9c-139">RELATED LINKS</span></span>

[<span data-ttu-id="6fe9c-140">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6fe9c-140">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)



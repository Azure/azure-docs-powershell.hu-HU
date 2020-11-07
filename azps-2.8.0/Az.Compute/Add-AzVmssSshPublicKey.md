---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 063b9fabb98b4c1370dcffa73fe2ecc664e0f0eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667498"
---
# <span data-ttu-id="dc2de-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="dc2de-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="dc2de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc2de-102">SYNOPSIS</span></span>
<span data-ttu-id="dc2de-103">Az SSH-beli nyilvános kulcsok felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="dc2de-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="dc2de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc2de-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc2de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc2de-105">DESCRIPTION</span></span>
<span data-ttu-id="dc2de-106">A **Add-AzVmssSshPublicKey** parancsmag hozzáadja azokat a nyilvános kulcsokat, amelyekkel a Virtual Machine Scale set (VMSS) Virtual Machines a biztonságos rendszerhéjon (SSH) keresztül csatlakozhat.</span><span class="sxs-lookup"><span data-stu-id="dc2de-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="dc2de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dc2de-107">EXAMPLES</span></span>

### <span data-ttu-id="dc2de-108">Példa 1: SSH-s nyilvános kulcs hozzáadása a VMSS</span><span class="sxs-lookup"><span data-stu-id="dc2de-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="dc2de-109">Ez a példa egy SSH-beli nyilvános kulcsot ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="dc2de-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="dc2de-110">Az első parancs a **New-AzVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dc2de-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="dc2de-111">A második parancs hozzáadja az SSH billentyűt a megadott kulccsal, és a virtuális gép megadott elérési útján tárolja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="dc2de-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="dc2de-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc2de-112">PARAMETERS</span></span>

### <span data-ttu-id="dc2de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc2de-113">-DefaultProfile</span></span>
<span data-ttu-id="dc2de-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc2de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc2de-115">-Adatforrások</span><span class="sxs-lookup"><span data-stu-id="dc2de-115">-KeyData</span></span>
<span data-ttu-id="dc2de-116">Az SSH RSA-beli nyilvános kulcsokra vonatkozó adatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc2de-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="dc2de-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="dc2de-117">-Path</span></span>
<span data-ttu-id="dc2de-118">A fájl teljes elérési útját adja meg a virtuális gépen, ahol ez a parancsmag az SSH-s nyilvános kulcsot tárolja.</span><span class="sxs-lookup"><span data-stu-id="dc2de-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="dc2de-119">Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="dc2de-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="dc2de-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dc2de-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="dc2de-121">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc2de-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="dc2de-122">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dc2de-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="dc2de-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc2de-123">-Confirm</span></span>
<span data-ttu-id="dc2de-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc2de-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc2de-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc2de-125">-WhatIf</span></span>
<span data-ttu-id="dc2de-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc2de-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc2de-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc2de-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc2de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc2de-128">CommonParameters</span></span>
<span data-ttu-id="dc2de-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc2de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc2de-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dc2de-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc2de-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc2de-131">INPUTS</span></span>

### <span data-ttu-id="dc2de-132">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dc2de-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="dc2de-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dc2de-133">System.String</span></span>

## <span data-ttu-id="dc2de-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc2de-134">OUTPUTS</span></span>

### <span data-ttu-id="dc2de-135">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="dc2de-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="dc2de-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc2de-136">NOTES</span></span>

## <span data-ttu-id="dc2de-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc2de-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc2de-138">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="dc2de-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 113af7a35ffee5960f4be6fe2fe989d9c1b36956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502767"
---
# <span data-ttu-id="a8da1-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a8da1-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="a8da1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8da1-102">SYNOPSIS</span></span>
<span data-ttu-id="a8da1-103">Az SSH-beli nyilvános kulcsok felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a8da1-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8da1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8da1-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8da1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8da1-105">DESCRIPTION</span></span>
<span data-ttu-id="a8da1-106">A **Add-AzureRmVmssSshPublicKey** parancsmag hozzáadja azokat a nyilvános kulcsokat, amelyekkel a Virtual Machine Scale set (VMSS) Virtual Machines a biztonságos rendszerhéjon (SSH) keresztül csatlakozhat.</span><span class="sxs-lookup"><span data-stu-id="a8da1-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="a8da1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8da1-107">EXAMPLES</span></span>

### <span data-ttu-id="a8da1-108">Példa 1: SSH-s nyilvános kulcs hozzáadása a VMSS</span><span class="sxs-lookup"><span data-stu-id="a8da1-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="a8da1-109">Ez a példa egy SSH-beli nyilvános kulcsot ad a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a8da1-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="a8da1-110">Az első parancs a **New-AzureRmVmssConfig** parancsmagot használja VMSS konfigurációs objektum létrehozásához, és az eredményt az $VMSS nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8da1-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="a8da1-111">A második parancs hozzáadja az SSH billentyűt a megadott kulccsal, és a virtuális gép megadott elérési útján tárolja a kulcsot.</span><span class="sxs-lookup"><span data-stu-id="a8da1-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="a8da1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8da1-112">PARAMETERS</span></span>

### <span data-ttu-id="a8da1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8da1-113">-DefaultProfile</span></span>
<span data-ttu-id="a8da1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8da1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8da1-115">-Adatforrások</span><span class="sxs-lookup"><span data-stu-id="a8da1-115">-KeyData</span></span>
<span data-ttu-id="a8da1-116">Az SSH RSA-beli nyilvános kulcsokra vonatkozó adatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8da1-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="a8da1-117">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a8da1-117">-Path</span></span>
<span data-ttu-id="a8da1-118">A fájl teljes elérési útját adja meg a virtuális gépen, ahol ez a parancsmag az SSH-s nyilvános kulcsot tárolja.</span><span class="sxs-lookup"><span data-stu-id="a8da1-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="a8da1-119">Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="a8da1-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="a8da1-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a8da1-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a8da1-121">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8da1-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="a8da1-122">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a8da1-122">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="a8da1-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a8da1-123">-Confirm</span></span>
<span data-ttu-id="a8da1-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a8da1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8da1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8da1-125">-WhatIf</span></span>
<span data-ttu-id="a8da1-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a8da1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8da1-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8da1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8da1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8da1-128">CommonParameters</span></span>
<span data-ttu-id="a8da1-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8da1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8da1-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8da1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8da1-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8da1-131">INPUTS</span></span>

## <span data-ttu-id="a8da1-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8da1-132">OUTPUTS</span></span>

###  
<span data-ttu-id="a8da1-133">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a8da1-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a8da1-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8da1-134">NOTES</span></span>

## <span data-ttu-id="a8da1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8da1-135">RELATED LINKS</span></span>

[<span data-ttu-id="a8da1-136">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a8da1-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182578"
---
# <span data-ttu-id="fc95d-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="fc95d-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="fc95d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc95d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc95d-103">A virtuális gép nyilvános kulcsait hozzáadja az SSH-hoz, ha csak a VM-et hozza létre.</span><span class="sxs-lookup"><span data-stu-id="fc95d-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="fc95d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc95d-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc95d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc95d-105">DESCRIPTION</span></span>
<span data-ttu-id="fc95d-106">A **Add-AzVMSshPublicKey** parancsmag hozzáadja azokat a nyilvános kulcsokat, amelyek segítségével a biztonságos rendszerhéjon (SSH) keresztül csatlakozhat egy linuxos virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="fc95d-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="fc95d-107">Ezt a problémát nem lehet használni a VM létrehozása után, ha ezt a problémát a VM-AzVM nélkül próbálja meg használni, nem jelenik meg hibaüzenet, ha a parancsot a Update-AzVM-val használja, a parancs hiba lép fel.</span><span class="sxs-lookup"><span data-stu-id="fc95d-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="fc95d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fc95d-108">EXAMPLES</span></span>

### <span data-ttu-id="fc95d-109">1. példa: nyilvános kulcs hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="fc95d-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="fc95d-110">Az első parancs a **Get-AzVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="fc95d-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="fc95d-111">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc95d-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fc95d-112">A második parancs hozzáadja a nyilvános kulcsot a VirtualMachine07 azon helyéhez, amelyen a Path paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="fc95d-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="fc95d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc95d-113">PARAMETERS</span></span>

### <span data-ttu-id="fc95d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc95d-114">-DefaultProfile</span></span>
<span data-ttu-id="fc95d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc95d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc95d-116">-Adatforrások</span><span class="sxs-lookup"><span data-stu-id="fc95d-116">-KeyData</span></span>
<span data-ttu-id="fc95d-117">A nyilvános kulcs 64-kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc95d-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="fc95d-118">Az SSH vagy a paraméter által megadott kulccsal csatlakozhat egy linuxos virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="fc95d-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc95d-119">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="fc95d-119">-Path</span></span>
<span data-ttu-id="fc95d-120">A fájl teljes elérési útját adja meg a virtuális gépen, ahol ez a parancsmag az SSH-s nyilvános kulcsot tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc95d-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="fc95d-121">Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="fc95d-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="fc95d-122">-VM</span><span class="sxs-lookup"><span data-stu-id="fc95d-122">-VM</span></span>
<span data-ttu-id="fc95d-123">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="fc95d-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="fc95d-124">Virtuális gép objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fc95d-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="fc95d-125">A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="fc95d-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc95d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc95d-126">CommonParameters</span></span>
<span data-ttu-id="fc95d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc95d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc95d-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fc95d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc95d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc95d-129">INPUTS</span></span>

### <span data-ttu-id="fc95d-130">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fc95d-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fc95d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fc95d-131">System.String</span></span>

## <span data-ttu-id="fc95d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc95d-132">OUTPUTS</span></span>

### <span data-ttu-id="fc95d-133">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fc95d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fc95d-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc95d-134">NOTES</span></span>

## <span data-ttu-id="fc95d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc95d-135">RELATED LINKS</span></span>

[<span data-ttu-id="fc95d-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fc95d-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="fc95d-137">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="fc95d-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

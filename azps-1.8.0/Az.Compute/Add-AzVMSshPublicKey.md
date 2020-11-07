---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 432de351ae62650ff4e4e2efae0550fab2fa6091
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671379"
---
# <span data-ttu-id="32e57-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="32e57-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="32e57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32e57-102">SYNOPSIS</span></span>
<span data-ttu-id="32e57-103">Hozzáadja az SSH-hoz szükséges nyilvános kulcsokat egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="32e57-103">Adds the public keys for SSH for a virtual machine.</span></span>

## <span data-ttu-id="32e57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32e57-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32e57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32e57-105">DESCRIPTION</span></span>
<span data-ttu-id="32e57-106">A **Add-AzVMSshPublicKey** parancsmag hozzáadja azokat a nyilvános kulcsokat, amelyekkel a biztonságos rendszerhéjon (SSH) keresztül csatlakozhat a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="32e57-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="32e57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="32e57-107">EXAMPLES</span></span>

### <span data-ttu-id="32e57-108">1. példa: nyilvános kulcs hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="32e57-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="32e57-109">Az első parancs a **Get-AzVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="32e57-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="32e57-110">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="32e57-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="32e57-111">A második parancs hozzáadja a nyilvános kulcsot a VirtualMachine07 azon helyéhez, amelyen a Path paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="32e57-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="32e57-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32e57-112">PARAMETERS</span></span>

### <span data-ttu-id="32e57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e57-113">-DefaultProfile</span></span>
<span data-ttu-id="32e57-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32e57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e57-115">-Adatforrások</span><span class="sxs-lookup"><span data-stu-id="32e57-115">-KeyData</span></span>
<span data-ttu-id="32e57-116">A nyilvános kulcs 64-kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="32e57-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="32e57-117">A virtuális gépeket az SSH segítségével vagy a paraméter által megadott kulcs használatával is elérheti.</span><span class="sxs-lookup"><span data-stu-id="32e57-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="32e57-118">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="32e57-118">-Path</span></span>
<span data-ttu-id="32e57-119">A fájl teljes elérési útját adja meg a virtuális gépen, ahol ez a parancsmag az SSH-s nyilvános kulcsot tárolja.</span><span class="sxs-lookup"><span data-stu-id="32e57-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="32e57-120">Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="32e57-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="32e57-121">-VM</span><span class="sxs-lookup"><span data-stu-id="32e57-121">-VM</span></span>
<span data-ttu-id="32e57-122">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="32e57-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="32e57-123">Virtuális gép objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="32e57-123">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="32e57-124">A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="32e57-124">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="32e57-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e57-125">CommonParameters</span></span>
<span data-ttu-id="32e57-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32e57-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e57-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e57-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e57-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32e57-128">INPUTS</span></span>

### <span data-ttu-id="32e57-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="32e57-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="32e57-130">System. String</span><span class="sxs-lookup"><span data-stu-id="32e57-130">System.String</span></span>

## <span data-ttu-id="32e57-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32e57-131">OUTPUTS</span></span>

### <span data-ttu-id="32e57-132">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="32e57-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="32e57-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32e57-133">NOTES</span></span>

## <span data-ttu-id="32e57-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32e57-134">RELATED LINKS</span></span>

[<span data-ttu-id="32e57-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="32e57-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="32e57-136">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="32e57-136">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

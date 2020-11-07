---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: b4cbc3ba7dd90d2810c4833fe1b74c13541fcb7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672387"
---
# <span data-ttu-id="29394-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="29394-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="29394-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29394-102">SYNOPSIS</span></span>
<span data-ttu-id="29394-103">Hozzáadja az SSH-hoz szükséges nyilvános kulcsokat egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="29394-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29394-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29394-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="29394-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29394-105">DESCRIPTION</span></span>
<span data-ttu-id="29394-106">A **Add-AzureRmVMSshPublicKey** parancsmag hozzáadja azokat a nyilvános kulcsokat, amelyekkel a biztonságos rendszerhéjon (SSH) keresztül csatlakozhat a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="29394-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="29394-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29394-107">EXAMPLES</span></span>

### <span data-ttu-id="29394-108">1. példa: nyilvános kulcs hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="29394-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="29394-109">Az első parancs a **Get-AzureRmVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="29394-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="29394-110">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="29394-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="29394-111">A második parancs hozzáadja a nyilvános kulcsot a VirtualMachine07 azon helyéhez, amelyen a Path paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="29394-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="29394-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29394-112">PARAMETERS</span></span>

### <span data-ttu-id="29394-113">-Adatforrások</span><span class="sxs-lookup"><span data-stu-id="29394-113">-KeyData</span></span>
<span data-ttu-id="29394-114">A nyilvános kulcs 64-kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="29394-114">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="29394-115">A virtuális gépeket az SSH segítségével vagy a paraméter által megadott kulcs használatával is elérheti.</span><span class="sxs-lookup"><span data-stu-id="29394-115">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="29394-116">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="29394-116">-Path</span></span>
<span data-ttu-id="29394-117">A fájl teljes elérési útját adja meg a virtuális gépen, ahol ez a parancsmag az SSH-s nyilvános kulcsot tárolja.</span><span class="sxs-lookup"><span data-stu-id="29394-117">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="29394-118">Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="29394-118">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="29394-119">-VM</span><span class="sxs-lookup"><span data-stu-id="29394-119">-VM</span></span>
<span data-ttu-id="29394-120">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="29394-120">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="29394-121">Virtuális gép objektum beszerzéséhez használja a [Get-AzureRmVM](./Get-AzureRmVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="29394-121">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="29394-122">A [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="29394-122">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29394-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29394-123">CommonParameters</span></span>
<span data-ttu-id="29394-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29394-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29394-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29394-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29394-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29394-126">INPUTS</span></span>

### <span data-ttu-id="29394-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="29394-127">None</span></span>
<span data-ttu-id="29394-128">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="29394-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29394-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29394-129">OUTPUTS</span></span>

## <span data-ttu-id="29394-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29394-130">NOTES</span></span>

## <span data-ttu-id="29394-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29394-131">RELATED LINKS</span></span>

[<span data-ttu-id="29394-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="29394-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="29394-133">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="29394-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

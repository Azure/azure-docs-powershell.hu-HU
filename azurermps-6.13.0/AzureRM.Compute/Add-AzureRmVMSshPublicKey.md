---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: 571d137e369cc997bce2b5a4f21839e64de8021a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673168"
---
# <span data-ttu-id="cd4a5-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="cd4a5-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="cd4a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4a5-103">Hozzáadja az SSH-hoz szükséges nyilvános kulcsokat egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd4a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd4a5-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd4a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd4a5-105">DESCRIPTION</span></span>
<span data-ttu-id="cd4a5-106">A **Add-AzureRmVMSshPublicKey** parancsmag hozzáadja azokat a nyilvános kulcsokat, amelyekkel a biztonságos rendszerhéjon (SSH) keresztül csatlakozhat a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="cd4a5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd4a5-107">EXAMPLES</span></span>

### <span data-ttu-id="cd4a5-108">1. példa: nyilvános kulcs hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="cd4a5-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="cd4a5-109">Az első parancs a **Get-AzureRmVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="cd4a5-110">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cd4a5-111">A második parancs hozzáadja a nyilvános kulcsot a VirtualMachine07 azon helyéhez, amelyen a Path paraméter van meghatározva.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="cd4a5-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd4a5-112">PARAMETERS</span></span>

### <span data-ttu-id="cd4a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4a5-113">-DefaultProfile</span></span>
<span data-ttu-id="cd4a5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd4a5-115">-Adatforrások</span><span class="sxs-lookup"><span data-stu-id="cd4a5-115">-KeyData</span></span>
<span data-ttu-id="cd4a5-116">A nyilvános kulcs 64-kódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="cd4a5-117">A virtuális gépeket az SSH segítségével vagy a paraméter által megadott kulcs használatával is elérheti.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="cd4a5-118">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="cd4a5-118">-Path</span></span>
<span data-ttu-id="cd4a5-119">A fájl teljes elérési útját adja meg a virtuális gépen, ahol ez a parancsmag az SSH-s nyilvános kulcsot tárolja.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="cd4a5-120">Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="cd4a5-121">-VM</span><span class="sxs-lookup"><span data-stu-id="cd4a5-121">-VM</span></span>
<span data-ttu-id="cd4a5-122">Azt a virtuálisgép-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="cd4a5-123">Virtuális gép objektum beszerzéséhez használja a [Get-AzureRmVM](./Get-AzureRmVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="cd4a5-124">A [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="cd4a5-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="cd4a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4a5-125">CommonParameters</span></span>
<span data-ttu-id="cd4a5-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd4a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4a5-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4a5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4a5-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd4a5-128">INPUTS</span></span>

### <span data-ttu-id="cd4a5-129">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cd4a5-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="cd4a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cd4a5-130">System.String</span></span>

## <span data-ttu-id="cd4a5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd4a5-131">OUTPUTS</span></span>

### <span data-ttu-id="cd4a5-132">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cd4a5-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cd4a5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd4a5-133">NOTES</span></span>

## <span data-ttu-id="cd4a5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd4a5-134">RELATED LINKS</span></span>

[<span data-ttu-id="cd4a5-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd4a5-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="cd4a5-136">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="cd4a5-136">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477885"
---
# <span data-ttu-id="d3633-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d3633-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="d3633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3633-102">SYNOPSIS</span></span>
<span data-ttu-id="d3633-103">Hozzáadja az SSH nyilvános kulcsait egy virtuális géphez, amikor csak a VM-et létrehozza.</span><span class="sxs-lookup"><span data-stu-id="d3633-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="d3633-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3633-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3633-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3633-105">DESCRIPTION</span></span>
<span data-ttu-id="d3633-106">Az **Add-AzVMSshPublicKey** parancsmag hozzáadja a Linux virtuális géphez a Secure Shell (SSH) rendszeren keresztüli csatlakozáshoz használható nyilvános kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="d3633-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="d3633-107">Ez nem használható a VM létrehozása után, ha azt követően próbálja használni ezt a hibát, hogy a VM update-AzVM nélküli létrehozása után nem jelenik meg hiba, ha az Update-AzVM paranccsal használja a parancsot, a parancs hibaüzenetet kap.</span><span class="sxs-lookup"><span data-stu-id="d3633-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="d3633-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3633-108">EXAMPLES</span></span>

### <span data-ttu-id="d3633-109">1. példa: Nyilvános kulcs hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="d3633-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="d3633-110">Az első parancs a VirtualMachine07 nevű virtuális gépet kapja meg **a Get-AzVM parancsmag** használatával.</span><span class="sxs-lookup"><span data-stu-id="d3633-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="d3633-111">A parancs a virtuális gépet a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="d3633-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d3633-112">A második parancs hozzáadja a nyilvános kulcsot a VirtualMachine07 azon helyhez, ahol a Path paraméter meg van adva.</span><span class="sxs-lookup"><span data-stu-id="d3633-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="d3633-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3633-113">PARAMETERS</span></span>

### <span data-ttu-id="d3633-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3633-114">-DefaultProfile</span></span>
<span data-ttu-id="d3633-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3633-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3633-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="d3633-116">-KeyData</span></span>
<span data-ttu-id="d3633-117">Egy nyilvános kulcs 64-es alapkódolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3633-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="d3633-118">Linuxos virtuális géphez csatlakozhat az SSH használatával vagy a paraméter által megadott kulcs használatával.</span><span class="sxs-lookup"><span data-stu-id="d3633-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3633-119">-Path</span><span class="sxs-lookup"><span data-stu-id="d3633-119">-Path</span></span>
<span data-ttu-id="d3633-120">Megadja egy fájl teljes elérési útját azon a virtuális gépen, ahol ez a parancsmag az SSH nyilvános kulcsot tárolja.</span><span class="sxs-lookup"><span data-stu-id="d3633-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="d3633-121">Ha a fájl már létezik, ez a parancsmag hozzáfűzi a kulcsot a fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="d3633-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="d3633-122">-VM</span><span class="sxs-lookup"><span data-stu-id="d3633-122">-VM</span></span>
<span data-ttu-id="d3633-123">Azt a virtuális gépobjektumot adja meg, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="d3633-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="d3633-124">Virtuális gépi objektum beszerzéséhez használja a [Get-AzVM](./Get-AzVM.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d3633-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="d3633-125">A [New-AzVMConfig](./New-AzVMConfig.md) parancsmaggal virtuális gépi objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="d3633-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="d3633-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3633-126">CommonParameters</span></span>
<span data-ttu-id="d3633-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3633-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3633-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3633-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3633-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3633-129">INPUTS</span></span>

### <span data-ttu-id="d3633-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d3633-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="d3633-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d3633-131">System.String</span></span>

## <span data-ttu-id="d3633-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3633-132">OUTPUTS</span></span>

### <span data-ttu-id="d3633-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d3633-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d3633-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3633-134">NOTES</span></span>

## <span data-ttu-id="d3633-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3633-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3633-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d3633-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d3633-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d3633-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015886"
---
# <span data-ttu-id="97830-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="97830-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="97830-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97830-102">SYNOPSIS</span></span>
<span data-ttu-id="97830-103">Virtuális gép alhálózatát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="97830-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="97830-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97830-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="97830-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97830-105">DESCRIPTION</span></span>
<span data-ttu-id="97830-106">A **New-WAPackVMSubnet** parancsmag létrehoz egy virtuális gép alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="97830-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="97830-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97830-107">EXAMPLES</span></span>

### <span data-ttu-id="97830-108">Példa 1: virtuális gép alhálózatának létrehozása</span><span class="sxs-lookup"><span data-stu-id="97830-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="97830-109">Az első parancs először kikeresi azt a virtuális gépet, amelyhez új virtuális gép alhálózatot szeretne felvenni.</span><span class="sxs-lookup"><span data-stu-id="97830-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="97830-110">Ez a virtuális gép hálózat neve ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="97830-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="97830-111">A második parancs a virtuális gép alhálózatát a korábban lekérdezett virtuális gép hálózata, a név ContosoVMSubnet01 és a 192.168.1.0/24 alhálózat segítségével hozza létre.</span><span class="sxs-lookup"><span data-stu-id="97830-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="97830-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97830-112">PARAMETERS</span></span>

### <span data-ttu-id="97830-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97830-113">-Name</span></span>
<span data-ttu-id="97830-114">A virtuális gép alhálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97830-114">Specifies a name for the virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97830-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="97830-115">-Profile</span></span>
<span data-ttu-id="97830-116">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="97830-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97830-117">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="97830-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97830-118">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="97830-118">-Subnet</span></span>
<span data-ttu-id="97830-119">A virtuális gép alhálózatának alhálózatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="97830-119">Specifies a subnet for the virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97830-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="97830-120">-VNet</span></span>
<span data-ttu-id="97830-121">A virtuális gép alhálózatához tartozó VNet adja meg.</span><span class="sxs-lookup"><span data-stu-id="97830-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97830-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97830-122">CommonParameters</span></span>
<span data-ttu-id="97830-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97830-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97830-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97830-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97830-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97830-125">INPUTS</span></span>

## <span data-ttu-id="97830-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97830-126">OUTPUTS</span></span>

## <span data-ttu-id="97830-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97830-127">NOTES</span></span>

## <span data-ttu-id="97830-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97830-128">RELATED LINKS</span></span>

[<span data-ttu-id="97830-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="97830-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="97830-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="97830-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="97830-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="97830-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)



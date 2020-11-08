---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017355"
---
# <span data-ttu-id="09b5b-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="09b5b-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="09b5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="09b5b-103">Virtuális gép alhálózati objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="09b5b-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="09b5b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09b5b-104">SYNTAX</span></span>

### <span data-ttu-id="09b5b-105">FromVMNetworkObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09b5b-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="09b5b-106">FromName</span><span class="sxs-lookup"><span data-stu-id="09b5b-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="09b5b-107">FromId</span><span class="sxs-lookup"><span data-stu-id="09b5b-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="09b5b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="09b5b-108">DESCRIPTION</span></span>
<span data-ttu-id="09b5b-109">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="09b5b-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="09b5b-110">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="09b5b-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="09b5b-111">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="09b5b-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="09b5b-112">A **Get-WAPackVMSubnet** parancsmag virtuális gép alhálózati objektumait kapja.</span><span class="sxs-lookup"><span data-stu-id="09b5b-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="09b5b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="09b5b-113">EXAMPLES</span></span>

### <span data-ttu-id="09b5b-114">Példa 1: virtuális gép alhálózatának beszerzése név használatával</span><span class="sxs-lookup"><span data-stu-id="09b5b-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="09b5b-115">Ez a parancs a ContosoSubnet01 nevű virtuális gép alhálózatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="09b5b-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="09b5b-116">2. példa: virtuális gép alhálózatának beszerzése azonosító használatával</span><span class="sxs-lookup"><span data-stu-id="09b5b-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="09b5b-117">Ez a parancs a megadott azonosítót tartalmazó virtuális gép alhálózatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="09b5b-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="09b5b-118">3. példa: az összes virtuális gép alhálózatának beszerzése egy adott virtualizált hálózatról</span><span class="sxs-lookup"><span data-stu-id="09b5b-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="09b5b-119">Ez a parancs egy adott virtualizált hálózatból kapja meg az összes virtuális gép alhálózatát.</span><span class="sxs-lookup"><span data-stu-id="09b5b-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="09b5b-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09b5b-120">PARAMETERS</span></span>

### <span data-ttu-id="09b5b-121">-AZONOSÍTÓ</span><span class="sxs-lookup"><span data-stu-id="09b5b-121">-ID</span></span>
<span data-ttu-id="09b5b-122">A virtuális gép alhálózat egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="09b5b-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b5b-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09b5b-123">-Name</span></span>
<span data-ttu-id="09b5b-124">Egy virtuális gép alhálózatának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09b5b-124">Specifies the name of a virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09b5b-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="09b5b-125">-Profile</span></span>
<span data-ttu-id="09b5b-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="09b5b-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="09b5b-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="09b5b-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="09b5b-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="09b5b-128">-VNet</span></span>
<span data-ttu-id="09b5b-129">A virtuális gép alhálózatához társított VNet adja meg.</span><span class="sxs-lookup"><span data-stu-id="09b5b-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

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

### <span data-ttu-id="09b5b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09b5b-130">CommonParameters</span></span>
<span data-ttu-id="09b5b-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09b5b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09b5b-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09b5b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09b5b-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09b5b-133">INPUTS</span></span>

## <span data-ttu-id="09b5b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09b5b-134">OUTPUTS</span></span>

## <span data-ttu-id="09b5b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09b5b-135">NOTES</span></span>

## <span data-ttu-id="09b5b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09b5b-136">RELATED LINKS</span></span>

[<span data-ttu-id="09b5b-137">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="09b5b-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="09b5b-138">Új – WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="09b5b-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="09b5b-139">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="09b5b-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)



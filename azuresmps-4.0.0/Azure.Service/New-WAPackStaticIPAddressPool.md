---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017381"
---
# <span data-ttu-id="3f75a-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f75a-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="3f75a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f75a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f75a-103">Statikus IP-címkészletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3f75a-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="3f75a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f75a-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f75a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f75a-105">DESCRIPTION</span></span>
<span data-ttu-id="3f75a-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="3f75a-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="3f75a-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="3f75a-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3f75a-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3f75a-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3f75a-109">A **New-WAPackStaticIPAddressPool** parancsmag egy statikus IP-címkészletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3f75a-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="3f75a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3f75a-110">EXAMPLES</span></span>

### <span data-ttu-id="3f75a-111">Példa 1: statikus IP-címkészlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="3f75a-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="3f75a-112">Az első parancs először kikeresi a virtuális gép hálózatát, amelyhez hozzá szeretné adni a statikus IP-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="3f75a-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="3f75a-113">Ez a virtuális gép hálózat neve ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="3f75a-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="3f75a-114">A második parancs a korábban lekérdezett virtuális gépet használja a ContosoVMSubnet01 nevű virtuális gép alhálózatának beszerzéséhez, amelyhez a statikus IP-címkészletet szeretné hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="3f75a-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="3f75a-115">A legutóbbi parancs új statikus IP-címkészletet hoz létre, amelynek neve ContosoStaticIpAddressPool01, az 192.168.1.0 és a tartományok végpontjának 192.168.1.10.</span><span class="sxs-lookup"><span data-stu-id="3f75a-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="3f75a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f75a-116">PARAMETERS</span></span>

### <span data-ttu-id="3f75a-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="3f75a-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="3f75a-118">A statikus IP-címkészlet IP-címtartomány végét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f75a-118">Specifies an IP address range end for the static IP address pool.</span></span>

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

### <span data-ttu-id="3f75a-119">-IPAddressRangeStart</span><span class="sxs-lookup"><span data-stu-id="3f75a-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="3f75a-120">Megadja az IP-címtartomány kezdetét a statikus IP-címkészlet számára.</span><span class="sxs-lookup"><span data-stu-id="3f75a-120">Specifies an IP address range start for the static IP address pool.</span></span>

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

### <span data-ttu-id="3f75a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f75a-121">-Name</span></span>
<span data-ttu-id="3f75a-122">A statikus IP-címkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f75a-122">Specifies a name for the static IP address pool.</span></span>

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

### <span data-ttu-id="3f75a-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f75a-123">-Profile</span></span>
<span data-ttu-id="3f75a-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3f75a-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f75a-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3f75a-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f75a-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="3f75a-126">-VMSubnet</span></span>
<span data-ttu-id="3f75a-127">A statikus IP-címkészlet által társított VMSubnet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3f75a-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f75a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f75a-128">CommonParameters</span></span>
<span data-ttu-id="3f75a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f75a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f75a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f75a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f75a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f75a-131">INPUTS</span></span>

## <span data-ttu-id="3f75a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f75a-132">OUTPUTS</span></span>

## <span data-ttu-id="3f75a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f75a-133">NOTES</span></span>

## <span data-ttu-id="3f75a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f75a-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f75a-135">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f75a-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="3f75a-136">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="3f75a-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017431"
---
# <span data-ttu-id="0590b-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="0590b-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="0590b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0590b-102">SYNOPSIS</span></span>
<span data-ttu-id="0590b-103">Statikus IP-címkészlet-objektumokat kap.</span><span class="sxs-lookup"><span data-stu-id="0590b-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="0590b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0590b-104">SYNTAX</span></span>

### <span data-ttu-id="0590b-105">FromVMSubnetObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0590b-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0590b-106">FromName</span><span class="sxs-lookup"><span data-stu-id="0590b-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="0590b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0590b-107">DESCRIPTION</span></span>
<span data-ttu-id="0590b-108">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="0590b-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="0590b-109">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="0590b-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0590b-110">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0590b-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0590b-111">A **Get-WAPackStaticIPAddressPool** parancsmag statikus IP-címkészlet-objektumokat kap.</span><span class="sxs-lookup"><span data-stu-id="0590b-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="0590b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0590b-112">EXAMPLES</span></span>

### <span data-ttu-id="0590b-113">Példa 1: statikus IP-címkészlet beszerzése egy adott VMSubnet</span><span class="sxs-lookup"><span data-stu-id="0590b-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="0590b-114">Ez a parancs a ContosoStaticIPAddressPool01 nevű statikus IP-címkészletet egy megadott VMSubnet kapja.</span><span class="sxs-lookup"><span data-stu-id="0590b-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="0590b-115">2. példa: a statikus IP-címkészlet beolvasása egy adott VMSubnet</span><span class="sxs-lookup"><span data-stu-id="0590b-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="0590b-116">Ez a parancs az összes statikus IP-készletet egy megadott VMSubet kapja.</span><span class="sxs-lookup"><span data-stu-id="0590b-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="0590b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0590b-117">PARAMETERS</span></span>

### <span data-ttu-id="0590b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0590b-118">-Name</span></span>
<span data-ttu-id="0590b-119">A statikus IP-címkészlet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0590b-119">Specifies the name of a static IP address pool.</span></span>

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

### <span data-ttu-id="0590b-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="0590b-120">-Profile</span></span>
<span data-ttu-id="0590b-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="0590b-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0590b-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="0590b-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0590b-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="0590b-123">-VMSubnet</span></span>
<span data-ttu-id="0590b-124">A statikus IP-címkészlet **VMSubnet** -objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0590b-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="0590b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0590b-125">CommonParameters</span></span>
<span data-ttu-id="0590b-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0590b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0590b-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0590b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0590b-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0590b-128">INPUTS</span></span>

## <span data-ttu-id="0590b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0590b-129">OUTPUTS</span></span>

## <span data-ttu-id="0590b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0590b-130">NOTES</span></span>

## <span data-ttu-id="0590b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0590b-131">RELATED LINKS</span></span>

[<span data-ttu-id="0590b-132">Új – WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="0590b-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="0590b-133">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="0590b-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017412"
---
# <span data-ttu-id="dea7c-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="dea7c-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="dea7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dea7c-102">SYNOPSIS</span></span>
<span data-ttu-id="dea7c-103">Eltávolítja a statikus IP-címkészlet objektumait.</span><span class="sxs-lookup"><span data-stu-id="dea7c-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="dea7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dea7c-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dea7c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dea7c-105">DESCRIPTION</span></span>
<span data-ttu-id="dea7c-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="dea7c-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="dea7c-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="dea7c-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="dea7c-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="dea7c-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="dea7c-109">A **Remove-WAPackStaticIPAddressPool** parancsmag eltávolítja a statikus IP-címkészlet objektumait.</span><span class="sxs-lookup"><span data-stu-id="dea7c-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="dea7c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="dea7c-110">EXAMPLES</span></span>

### <span data-ttu-id="dea7c-111">1. példa: statikus IP-címkészlet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dea7c-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="dea7c-112">Az első parancs a **Get-WAPackStaticIPAddressPool** parancsmaggal a ContosoStaticIPAddressPool01 nevű statikus IP-címkészletet kapja, majd az objektumot a $StaticIPAddressPool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dea7c-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="dea7c-113">A második parancs eltávolítja a $StaticIPAddressPoolban tárolt statikus IP-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="dea7c-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="dea7c-114">A parancs a megerősítést kéri.</span><span class="sxs-lookup"><span data-stu-id="dea7c-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="dea7c-115">2. példa: statikus IP-címkészlet eltávolítása megerősítés nélkül</span><span class="sxs-lookup"><span data-stu-id="dea7c-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="dea7c-116">Az első parancs a **Get-WAPackStaticIPAddressPool** parancsmaggal a ContosoStaticIPAddressPool02 nevű statikus IP-címkészletet kapja, majd az objektumot a $ StaticIPAddressPool változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="dea7c-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="dea7c-117">A második parancs eltávolítja a $StaticIPAddressPoolban tárolt statikus IP-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="dea7c-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="dea7c-118">Ez a parancs az *erő* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dea7c-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="dea7c-119">A parancs nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dea7c-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dea7c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dea7c-120">PARAMETERS</span></span>

### <span data-ttu-id="dea7c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dea7c-121">-Force</span></span>
<span data-ttu-id="dea7c-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="dea7c-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea7c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dea7c-123">-PassThru</span></span>
<span data-ttu-id="dea7c-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="dea7c-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dea7c-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="dea7c-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dea7c-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="dea7c-126">-Profile</span></span>
<span data-ttu-id="dea7c-127">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="dea7c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dea7c-128">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="dea7c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dea7c-129">-StaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="dea7c-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="dea7c-130">Megadja a StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="dea7c-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="dea7c-131">Ha statikus IP-címkészletet szeretne beolvasni, használja a **Get-WAPackStaticIPAddressPool** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dea7c-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dea7c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea7c-132">CommonParameters</span></span>
<span data-ttu-id="dea7c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dea7c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea7c-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dea7c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea7c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea7c-135">INPUTS</span></span>

## <span data-ttu-id="dea7c-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dea7c-136">OUTPUTS</span></span>

## <span data-ttu-id="dea7c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dea7c-137">NOTES</span></span>

## <span data-ttu-id="dea7c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dea7c-138">RELATED LINKS</span></span>

[<span data-ttu-id="dea7c-139">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="dea7c-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="dea7c-140">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="dea7c-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)



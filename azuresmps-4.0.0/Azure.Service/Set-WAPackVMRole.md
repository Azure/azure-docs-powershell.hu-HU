---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017383"
---
# <span data-ttu-id="14c71-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="14c71-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="14c71-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14c71-102">SYNOPSIS</span></span>
<span data-ttu-id="14c71-103">Módosítja egy virtuális gép szerepkör példányának Count tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="14c71-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="14c71-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14c71-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="14c71-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14c71-105">DESCRIPTION</span></span>
<span data-ttu-id="14c71-106">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="14c71-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="14c71-107">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="14c71-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="14c71-108">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="14c71-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="14c71-109">A **set-WAPackVMRole** parancsmag a virtuálisgép-szerepkörök példányai tulajdonságát módosítja.</span><span class="sxs-lookup"><span data-stu-id="14c71-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="14c71-110">Példák</span><span class="sxs-lookup"><span data-stu-id="14c71-110">EXAMPLES</span></span>

### <span data-ttu-id="14c71-111">Példa 1: a virtuálisgép-szerepkörök előfordulási számának megadása</span><span class="sxs-lookup"><span data-stu-id="14c71-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="14c71-112">Az első parancs megkapja a ContosoVMRole01 nevű virtuális gép szerepkört a **Get-WAPackVMRole** parancsmaggal, majd az objektumot a $VMRole változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="14c71-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="14c71-113">A második és a végleges parancs a virtuális gép új példányának számát állítja be $VMRole-ról 3-ra.</span><span class="sxs-lookup"><span data-stu-id="14c71-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="14c71-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14c71-114">PARAMETERS</span></span>

### <span data-ttu-id="14c71-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="14c71-115">-InstanceCount</span></span>
<span data-ttu-id="14c71-116">Egy virtuális gép szerepkör példányának számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="14c71-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c71-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14c71-117">-PassThru</span></span>
<span data-ttu-id="14c71-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="14c71-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="14c71-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="14c71-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14c71-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="14c71-120">-Profile</span></span>
<span data-ttu-id="14c71-121">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="14c71-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="14c71-122">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="14c71-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="14c71-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="14c71-123">-VMRole</span></span>
<span data-ttu-id="14c71-124">Virtuális gép szerepkört ad meg.</span><span class="sxs-lookup"><span data-stu-id="14c71-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="14c71-125">A Virtual Machine szerepkör beszerzéséhez használja a **Get-WAPackVMRole** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="14c71-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c71-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c71-126">CommonParameters</span></span>
<span data-ttu-id="14c71-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14c71-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c71-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c71-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c71-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14c71-129">INPUTS</span></span>

## <span data-ttu-id="14c71-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14c71-130">OUTPUTS</span></span>

## <span data-ttu-id="14c71-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14c71-131">NOTES</span></span>

## <span data-ttu-id="14c71-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14c71-132">RELATED LINKS</span></span>

[<span data-ttu-id="14c71-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="14c71-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="14c71-134">Új – WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="14c71-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="14c71-135">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="14c71-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)



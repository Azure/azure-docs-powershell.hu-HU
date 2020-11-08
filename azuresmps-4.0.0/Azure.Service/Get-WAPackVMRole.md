---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94017414"
---
# <span data-ttu-id="ab1e2-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="ab1e2-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="ab1e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab1e2-102">SYNOPSIS</span></span>

## <span data-ttu-id="ab1e2-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab1e2-103">SYNTAX</span></span>

### <span data-ttu-id="ab1e2-104">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab1e2-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ab1e2-105">FromName</span><span class="sxs-lookup"><span data-stu-id="ab1e2-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ab1e2-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="ab1e2-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ab1e2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab1e2-107">DESCRIPTION</span></span>
<span data-ttu-id="ab1e2-108">Ezek a témakörök elavultak, és a jövőben törlődnek.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ab1e2-109">Ez a témakör a Microsoft Azure PowerShell modul 0.8.1 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ab1e2-110">A használt modul verziójának megkereséséhez írja be a következőt az Azure PowerShell konzolból `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ab1e2-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="ab1e2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ab1e2-111">EXAMPLES</span></span>

### <span data-ttu-id="ab1e2-112">Példa 1: virtuális gép szerepkör beszerzése (a portálon keresztül létrehozva)</span><span class="sxs-lookup"><span data-stu-id="ab1e2-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="ab1e2-113">Ez a parancs a ContosoVMRole01 nevű portálon keresztül létrehozott virtuális gép szerepkört kapja.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="ab1e2-114">2. példa: virtuális gép szerepkör beszerzése név és Felhőbeli szolgáltatás nevének használatával</span><span class="sxs-lookup"><span data-stu-id="ab1e2-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="ab1e2-115">Ez a parancs a ContosoVMRole02 nevű virtuális gép szerepkört kapja, amely a ContosoCloudService01 nevű felhő-szolgáltatásra áll.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="ab1e2-116">3. példa: az összes virtuális gép szerepkör beszerzése</span><span class="sxs-lookup"><span data-stu-id="ab1e2-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="ab1e2-117">Ez a parancs a meglévő virtuális gép szerepkört kapja.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="ab1e2-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab1e2-118">PARAMETERS</span></span>

### <span data-ttu-id="ab1e2-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ab1e2-119">-CloudServiceName</span></span>
<span data-ttu-id="ab1e2-120">A virtuális gép szerepkör Felhőbeli szolgáltatásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab1e2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ab1e2-121">-Name</span></span>
<span data-ttu-id="ab1e2-122">A virtuális gép szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab1e2-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="ab1e2-123">-Profile</span></span>
<span data-ttu-id="ab1e2-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ab1e2-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ab1e2-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ab1e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1e2-126">CommonParameters</span></span>
<span data-ttu-id="ab1e2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab1e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1e2-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab1e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1e2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab1e2-129">INPUTS</span></span>

## <span data-ttu-id="ab1e2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab1e2-130">OUTPUTS</span></span>

## <span data-ttu-id="ab1e2-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab1e2-131">NOTES</span></span>

## <span data-ttu-id="ab1e2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab1e2-132">RELATED LINKS</span></span>

[<span data-ttu-id="ab1e2-133">Új – WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="ab1e2-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="ab1e2-134">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="ab1e2-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="ab1e2-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="ab1e2-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)



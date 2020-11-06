---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: fc9d8db7f293ff94e33b50afd55176d157046fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499164"
---
# <span data-ttu-id="038eb-101">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="038eb-101">Get-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="038eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="038eb-102">SYNOPSIS</span></span>
<span data-ttu-id="038eb-103">Beolvassa a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="038eb-103">Gets the login credentials for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="038eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="038eb-104">SYNTAX</span></span>

### <span data-ttu-id="038eb-105">NameResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="038eb-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="038eb-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="038eb-106">RegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="038eb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="038eb-107">DESCRIPTION</span></span>
<span data-ttu-id="038eb-108">A **Get-AzureRmContainerRegistryCredential** parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="038eb-108">The **Get-AzureRmContainerRegistryCredential** cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="038eb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="038eb-109">EXAMPLES</span></span>

### <span data-ttu-id="038eb-110">Példa 1: bejelentkezési hitelesítő adatok beszerzése a tároló beállításjegyzékéhez</span><span class="sxs-lookup"><span data-stu-id="038eb-110">Example 1: Get the login credentials for a container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="038eb-111">Ez a parancs a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="038eb-111">This command gets the login credentials for the specified container registry.</span></span> <span data-ttu-id="038eb-112">A `MyRegistry` hitelesítő adatok beszerzéséhez rendszergazdai jogosultsággal kell rendelkezni a rendszergazda számára a tároló beállításjegyzékének engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="038eb-112">Admin user has to be enabled for the container registry `MyRegistry` to get login credentials.</span></span>

## <span data-ttu-id="038eb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="038eb-113">PARAMETERS</span></span>

### <span data-ttu-id="038eb-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="038eb-114">-Name</span></span>
<span data-ttu-id="038eb-115">A tároló beállításjegyzékének neve.</span><span class="sxs-lookup"><span data-stu-id="038eb-115">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038eb-116">-Registry</span><span class="sxs-lookup"><span data-stu-id="038eb-116">-Registry</span></span>
<span data-ttu-id="038eb-117">Tároló rendszerleíróadatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="038eb-117">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="038eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038eb-118">-ResourceGroupName</span></span>
<span data-ttu-id="038eb-119">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="038eb-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038eb-120">-DefaultProfile</span></span>
<span data-ttu-id="038eb-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="038eb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="038eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038eb-122">CommonParameters</span></span>
<span data-ttu-id="038eb-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="038eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038eb-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="038eb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038eb-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="038eb-125">INPUTS</span></span>

### <span data-ttu-id="038eb-126">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="038eb-126">PSContainerRegistry</span></span>
<span data-ttu-id="038eb-127">A "Registry" paraméter elfogadja a "PSContainerRegistry" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="038eb-127">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="038eb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="038eb-128">OUTPUTS</span></span>

### <span data-ttu-id="038eb-129">Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="038eb-129">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="038eb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="038eb-130">NOTES</span></span>

## <span data-ttu-id="038eb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="038eb-131">RELATED LINKS</span></span>

[<span data-ttu-id="038eb-132">Új – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="038eb-132">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="038eb-133">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="038eb-133">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="038eb-134">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="038eb-134">Update-AzureRmContainerRegistryCredential</span></span>](./Update-AzureRmContainerRegistryCredential.md)


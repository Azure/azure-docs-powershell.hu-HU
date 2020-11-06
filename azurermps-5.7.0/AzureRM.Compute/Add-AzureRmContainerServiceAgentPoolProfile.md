---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499048"
---
# <span data-ttu-id="cfd1f-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="cfd1f-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="cfd1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd1f-103">Elhelyez egy tároló szolgáltatás-ügynök készlet-profilt.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfd1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfd1f-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd1f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfd1f-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd1f-106">Az **Add-AzureRmContainerServiceAgentPoolProfile** parancsmag a Container Service Agent Pool-profilját hozzáadja egy helyi tároló szolgáltatási objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="cfd1f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cfd1f-107">EXAMPLES</span></span>

### <span data-ttu-id="cfd1f-108">1. példa: profil hozzáadása</span><span class="sxs-lookup"><span data-stu-id="cfd1f-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="cfd1f-109">Ez a parancs hozzáadja a Container Service Agent Pool-profilját a local Container Service objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="cfd1f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfd1f-110">PARAMETERS</span></span>

### <span data-ttu-id="cfd1f-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="cfd1f-111">-ContainerService</span></span>
<span data-ttu-id="cfd1f-112">Annak a tároló-szolgáltatás objektumnak a megadása, amelyhez a parancsmag hozzáadja az Agent Pool-profilt.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="cfd1f-113">**ContainerService** -objektum beolvasásához használja a [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd1f-114">-Count</span><span class="sxs-lookup"><span data-stu-id="cfd1f-114">-Count</span></span>
<span data-ttu-id="cfd1f-115">A szállítótartályokat tároló ügynökök számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="cfd1f-116">A paraméter elfogadható értékei a következők: 1 – 100-ig terjedő egész számok.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="cfd1f-117">Az alapértelmezett érték 1.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-117">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd1f-118">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="cfd1f-118">-DnsPrefix</span></span>
<span data-ttu-id="cfd1f-119">Azt a DNS-előtagot adja meg, amelyet a parancsmag a teljes tartománynevet használja az ügynöki készlet számára.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-119">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd1f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cfd1f-120">-Name</span></span>
<span data-ttu-id="cfd1f-121">Az Agent Pool-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-121">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="cfd1f-122">Ennek az értéknek egyedinek kell lennie az előfizetés és az erőforráscsoport kontextusában.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-122">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd1f-123">-VmSize</span><span class="sxs-lookup"><span data-stu-id="cfd1f-123">-VmSize</span></span>
<span data-ttu-id="cfd1f-124">A meghatalmazottak virtuális gépei méretének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-124">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd1f-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cfd1f-125">-Confirm</span></span>
<span data-ttu-id="cfd1f-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd1f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd1f-127">-WhatIf</span></span>
<span data-ttu-id="cfd1f-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfd1f-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd1f-130">CommonParameters</span></span>
<span data-ttu-id="cfd1f-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfd1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd1f-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd1f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd1f-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfd1f-133">INPUTS</span></span>

### <span data-ttu-id="cfd1f-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="cfd1f-134">None</span></span>
<span data-ttu-id="cfd1f-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cfd1f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cfd1f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfd1f-136">OUTPUTS</span></span>

## <span data-ttu-id="cfd1f-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfd1f-137">NOTES</span></span>

## <span data-ttu-id="cfd1f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfd1f-138">RELATED LINKS</span></span>

[<span data-ttu-id="cfd1f-139">Új – AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="cfd1f-139">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="cfd1f-140">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="cfd1f-140">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)

---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: 62acfacbafb50f85673b37e802b9d0b0eb4bf66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492344"
---
# <span data-ttu-id="cdacd-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cdacd-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="cdacd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cdacd-102">SYNOPSIS</span></span>
<span data-ttu-id="cdacd-103">Frissíti a tároló szolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="cdacd-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdacd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cdacd-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdacd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cdacd-105">DESCRIPTION</span></span>
<span data-ttu-id="cdacd-106">Az **Update-AzureRmContainerService** parancsmag frissíti a tároló szolgáltatás állapotát a szolgáltatás helyi példányának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="cdacd-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="cdacd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cdacd-107">EXAMPLES</span></span>

### <span data-ttu-id="cdacd-108">Példa 1: tároló szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="cdacd-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="cdacd-109">Ez a parancs a CSResourceGroup17 nevű tároló szolgáltatást az Get-AzureRmContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cdacd-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="cdacd-110">A parancs a pipeline operátor segítségével átadja az objektumot az Remove-AzureRmContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cdacd-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="cdacd-111">**Remove-AzureRmContainerServiceAgentPoolProfile –** eltávolítja a AgentPool01 nevű profilt.</span><span class="sxs-lookup"><span data-stu-id="cdacd-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="cdacd-112">A parancs átadja az eredményt az Add-AzureRmContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cdacd-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="cdacd-113">A **Add-AzureRmContainerServiceAgentPoolProfile** felveszi a AgentPool01 nevű profilt, és a megadott tulajdonságokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cdacd-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="cdacd-114">A parancs átadja az eredményt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="cdacd-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="cdacd-115">Az aktuális parancsmag frissíti a tároló szolgáltatást a parancsban elvégzett módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="cdacd-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="cdacd-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cdacd-116">PARAMETERS</span></span>

### <span data-ttu-id="cdacd-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="cdacd-117">-ContainerService</span></span>
<span data-ttu-id="cdacd-118">Egy olyan helyi **ContainerService** -objektumot ad meg, amely módosításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="cdacd-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdacd-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cdacd-119">-Name</span></span>
<span data-ttu-id="cdacd-120">Annak a tároló szolgáltatásnak a nevét adja meg, amelyre a parancsmag frissíti.</span><span class="sxs-lookup"><span data-stu-id="cdacd-120">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdacd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdacd-121">-ResourceGroupName</span></span>
<span data-ttu-id="cdacd-122">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="cdacd-122">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdacd-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cdacd-123">-Confirm</span></span>
<span data-ttu-id="cdacd-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cdacd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdacd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdacd-125">-WhatIf</span></span>
<span data-ttu-id="cdacd-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cdacd-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cdacd-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cdacd-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdacd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdacd-128">CommonParameters</span></span>
<span data-ttu-id="cdacd-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cdacd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdacd-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdacd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdacd-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdacd-131">INPUTS</span></span>

### <span data-ttu-id="cdacd-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="cdacd-132">None</span></span>
<span data-ttu-id="cdacd-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cdacd-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cdacd-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdacd-134">OUTPUTS</span></span>

## <span data-ttu-id="cdacd-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cdacd-135">NOTES</span></span>

## <span data-ttu-id="cdacd-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdacd-136">RELATED LINKS</span></span>

[<span data-ttu-id="cdacd-137">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="cdacd-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="cdacd-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cdacd-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="cdacd-139">Új – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cdacd-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="cdacd-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cdacd-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="cdacd-141">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="cdacd-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)



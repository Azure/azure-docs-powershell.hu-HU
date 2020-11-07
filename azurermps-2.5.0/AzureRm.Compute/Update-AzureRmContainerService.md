---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850870"
---
# <span data-ttu-id="310c5-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="310c5-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="310c5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="310c5-102">SYNOPSIS</span></span>
<span data-ttu-id="310c5-103">Frissíti a tároló szolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="310c5-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="310c5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="310c5-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="310c5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="310c5-105">DESCRIPTION</span></span>
<span data-ttu-id="310c5-106">Az **Update-AzureRmContainerService** parancsmag frissíti a tároló szolgáltatás állapotát a szolgáltatás helyi példányának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="310c5-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="310c5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="310c5-107">EXAMPLES</span></span>

### <span data-ttu-id="310c5-108">Példa 1: tároló szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="310c5-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="310c5-109">Ez a parancs a CSResourceGroup17 nevű tároló szolgáltatást az Get-AzureRmContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="310c5-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="310c5-110">A parancs a pipeline operátor segítségével átadja az objektumot az Remove-AzureRmContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="310c5-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="310c5-111">**Remove-AzureRmContainerServiceAgentPoolProfile –** eltávolítja a AgentPool01 nevű profilt.</span><span class="sxs-lookup"><span data-stu-id="310c5-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="310c5-112">A parancs átadja az eredményt az Add-AzureRmContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="310c5-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="310c5-113">A **Add-AzureRmContainerServiceAgentPoolProfile** felveszi a AgentPool01 nevű profilt, és a megadott tulajdonságokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="310c5-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="310c5-114">A parancs átadja az eredményt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="310c5-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="310c5-115">Az aktuális parancsmag frissíti a tároló szolgáltatást a parancsban elvégzett módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="310c5-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="310c5-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="310c5-116">PARAMETERS</span></span>

### <span data-ttu-id="310c5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="310c5-117">-AsJob</span></span>
<span data-ttu-id="310c5-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="310c5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="310c5-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="310c5-119">-ContainerService</span></span>
<span data-ttu-id="310c5-120">Egy olyan helyi **ContainerService** -objektumot ad meg, amely módosításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="310c5-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="310c5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310c5-121">-DefaultProfile</span></span>
<span data-ttu-id="310c5-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="310c5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310c5-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="310c5-123">-Name</span></span>
<span data-ttu-id="310c5-124">Annak a tároló szolgáltatásnak a nevét adja meg, amelyre a parancsmag frissíti.</span><span class="sxs-lookup"><span data-stu-id="310c5-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="310c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="310c5-126">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="310c5-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="310c5-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="310c5-127">-Confirm</span></span>
<span data-ttu-id="310c5-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="310c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310c5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310c5-129">-WhatIf</span></span>
<span data-ttu-id="310c5-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="310c5-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="310c5-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="310c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310c5-132">CommonParameters</span></span>
<span data-ttu-id="310c5-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="310c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310c5-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310c5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310c5-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="310c5-135">INPUTS</span></span>

### <span data-ttu-id="310c5-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="310c5-136">ContainerService</span></span>
<span data-ttu-id="310c5-137">A ' ContainerService ' paraméter az "ContainerService" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="310c5-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="310c5-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="310c5-138">OUTPUTS</span></span>

### <span data-ttu-id="310c5-139">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="310c5-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="310c5-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="310c5-140">NOTES</span></span>

## <span data-ttu-id="310c5-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="310c5-141">RELATED LINKS</span></span>

[<span data-ttu-id="310c5-142">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="310c5-142">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="310c5-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="310c5-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="310c5-144">Új – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="310c5-144">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="310c5-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="310c5-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="310c5-146">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="310c5-146">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)



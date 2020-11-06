---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: ca6a89f7818760a6bab65e45fec703c00d8e7f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505135"
---
# <span data-ttu-id="f323c-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f323c-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="f323c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f323c-102">SYNOPSIS</span></span>
<span data-ttu-id="f323c-103">Frissíti a tároló szolgáltatás állapotát.</span><span class="sxs-lookup"><span data-stu-id="f323c-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f323c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f323c-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f323c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f323c-105">DESCRIPTION</span></span>
<span data-ttu-id="f323c-106">Az **Update-AzureRmContainerService** parancsmag frissíti a tároló szolgáltatás állapotát a szolgáltatás helyi példányának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="f323c-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="f323c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f323c-107">EXAMPLES</span></span>

### <span data-ttu-id="f323c-108">Példa 1: tároló szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="f323c-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="f323c-109">Ez a parancs a CSResourceGroup17 nevű tároló szolgáltatást az Get-AzureRmContainerService parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f323c-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="f323c-110">A parancs a pipeline operátor segítségével átadja az objektumot az Remove-AzureRmContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="f323c-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="f323c-111">**Remove-AzureRmContainerServiceAgentPoolProfile –** eltávolítja a AgentPool01 nevű profilt.</span><span class="sxs-lookup"><span data-stu-id="f323c-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="f323c-112">A parancs átadja az eredményt az Add-AzureRmContainerServiceAgentPoolProfile parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="f323c-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="f323c-113">A **Add-AzureRmContainerServiceAgentPoolProfile** felveszi a AgentPool01 nevű profilt, és a megadott tulajdonságokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f323c-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="f323c-114">A parancs átadja az eredményt az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="f323c-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="f323c-115">Az aktuális parancsmag frissíti a tároló szolgáltatást a parancsban elvégzett módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="f323c-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="f323c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f323c-116">PARAMETERS</span></span>

### <span data-ttu-id="f323c-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="f323c-117">-ContainerService</span></span>
<span data-ttu-id="f323c-118">Egy olyan helyi **ContainerService** -objektumot ad meg, amely módosításokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="f323c-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f323c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f323c-119">-DefaultProfile</span></span>
<span data-ttu-id="f323c-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f323c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f323c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f323c-121">-Name</span></span>
<span data-ttu-id="f323c-122">Annak a tároló szolgáltatásnak a nevét adja meg, amelyre a parancsmag frissíti.</span><span class="sxs-lookup"><span data-stu-id="f323c-122">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f323c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f323c-123">-ResourceGroupName</span></span>
<span data-ttu-id="f323c-124">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amelyet a parancsmag frissít.</span><span class="sxs-lookup"><span data-stu-id="f323c-124">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f323c-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f323c-125">-Confirm</span></span>
<span data-ttu-id="f323c-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f323c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f323c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f323c-127">-WhatIf</span></span>
<span data-ttu-id="f323c-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f323c-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f323c-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f323c-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f323c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f323c-130">CommonParameters</span></span>
<span data-ttu-id="f323c-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f323c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f323c-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f323c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f323c-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f323c-133">INPUTS</span></span>

## <span data-ttu-id="f323c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f323c-134">OUTPUTS</span></span>

## <span data-ttu-id="f323c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f323c-135">NOTES</span></span>

## <span data-ttu-id="f323c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f323c-136">RELATED LINKS</span></span>

[<span data-ttu-id="f323c-137">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f323c-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="f323c-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f323c-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="f323c-139">Új – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f323c-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="f323c-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f323c-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="f323c-141">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f323c-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)



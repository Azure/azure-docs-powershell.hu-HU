---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 909121a78d09db7d15591a93db9479d0ccc8381b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500315"
---
# <span data-ttu-id="ff4f7-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="ff4f7-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="ff4f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4f7-103">Felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="ff4f7-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff4f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff4f7-104">SYNTAX</span></span>

### <span data-ttu-id="ff4f7-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff4f7-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff4f7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff4f7-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff4f7-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff4f7-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff4f7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff4f7-108">DESCRIPTION</span></span>
<span data-ttu-id="ff4f7-109">Felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="ff4f7-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ff4f7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ff4f7-110">EXAMPLES</span></span>

### <span data-ttu-id="ff4f7-111">Meglévő felügyelt Kubernetes-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="ff4f7-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="ff4f7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff4f7-112">PARAMETERS</span></span>

### <span data-ttu-id="ff4f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff4f7-113">-AsJob</span></span>
<span data-ttu-id="ff4f7-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ff4f7-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4f7-115">-DefaultProfile</span></span>
<span data-ttu-id="ff4f7-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff4f7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ff4f7-117">-Force</span></span>
<span data-ttu-id="ff4f7-118">Felügyelt Kubernetes-fürt eltávolítása üzenet nélkül</span><span class="sxs-lookup"><span data-stu-id="ff4f7-118">Remove managed Kubernetes cluster without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ff4f7-119">-Id</span></span>
<span data-ttu-id="ff4f7-120">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="ff4f7-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff4f7-121">-InputObject</span></span>
<span data-ttu-id="ff4f7-122">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff4f7-123">-Name</span></span>
<span data-ttu-id="ff4f7-124">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="ff4f7-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff4f7-125">-PassThru</span></span>
<span data-ttu-id="ff4f7-126">Eredménye igaz, ha a törlés sikeres</span><span class="sxs-lookup"><span data-stu-id="ff4f7-126">Returns true if deletion is successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff4f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="ff4f7-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ff4f7-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff4f7-129">-Confirm</span></span>
<span data-ttu-id="ff4f7-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff4f7-131">-WhatIf</span></span>
<span data-ttu-id="ff4f7-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff4f7-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff4f7-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff4f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4f7-134">CommonParameters</span></span>
<span data-ttu-id="ff4f7-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff4f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4f7-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff4f7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4f7-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff4f7-137">INPUTS</span></span>

### <span data-ttu-id="ff4f7-138">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ff4f7-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="ff4f7-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff4f7-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ff4f7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ff4f7-140">System.String</span></span>

## <span data-ttu-id="ff4f7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff4f7-141">OUTPUTS</span></span>

### <span data-ttu-id="ff4f7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff4f7-142">System.Boolean</span></span>

## <span data-ttu-id="ff4f7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff4f7-143">NOTES</span></span>

## <span data-ttu-id="ff4f7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff4f7-144">RELATED LINKS</span></span>

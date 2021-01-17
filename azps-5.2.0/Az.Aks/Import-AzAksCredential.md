---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348017"
---
# <span data-ttu-id="9cc81-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="9cc81-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="9cc81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cc81-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc81-103">Felügyelt Kutectl-konstúgó importálása és egyesítése felügyelt Kubanetes-fürthöz</span><span class="sxs-lookup"><span data-stu-id="9cc81-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="9cc81-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9cc81-104">SYNTAX</span></span>

### <span data-ttu-id="9cc81-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cc81-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc81-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cc81-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc81-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cc81-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cc81-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9cc81-108">DESCRIPTION</span></span>
<span data-ttu-id="9cc81-109">Felügyelt Kutectl-konstúgó importálása és egyesítése felügyelt Kubanetes-fürthöz</span><span class="sxs-lookup"><span data-stu-id="9cc81-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="9cc81-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9cc81-110">EXAMPLES</span></span>

### <span data-ttu-id="9cc81-111">A Kutectl-konfiguráció importálása és egyesítése</span><span class="sxs-lookup"><span data-stu-id="9cc81-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="9cc81-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cc81-112">PARAMETERS</span></span>

### <span data-ttu-id="9cc81-113">- Rendszergazda</span><span class="sxs-lookup"><span data-stu-id="9cc81-113">-Admin</span></span>
<span data-ttu-id="9cc81-114">Az alapértelmezett "clusterUser" helyett a "clusterAdmin" kutectl config fájlhoz jut.</span><span class="sxs-lookup"><span data-stu-id="9cc81-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="9cc81-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="9cc81-115">-ConfigPath</span></span>
<span data-ttu-id="9cc81-116">Egy létrehozni vagy frissíteni kívánt konfigurációs fájl.</span><span class="sxs-lookup"><span data-stu-id="9cc81-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="9cc81-117">A YAML-fájl nyomtatása stdout formátumban a "-" használatával.</span><span class="sxs-lookup"><span data-stu-id="9cc81-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="9cc81-118">Alapértelmezett: %Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="9cc81-118">Default: %Home%/.kube/config.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc81-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc81-119">-DefaultProfile</span></span>
<span data-ttu-id="9cc81-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cc81-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc81-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9cc81-121">-Force</span></span>
<span data-ttu-id="9cc81-122">Import Kubernetes config even if it is the default</span><span class="sxs-lookup"><span data-stu-id="9cc81-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="9cc81-123">-Id</span><span class="sxs-lookup"><span data-stu-id="9cc81-123">-Id</span></span>
<span data-ttu-id="9cc81-124">Felügyelt Kubanetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="9cc81-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9cc81-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cc81-125">-InputObject</span></span>
<span data-ttu-id="9cc81-126">EGY PSKubernetesCluster-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="9cc81-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="9cc81-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9cc81-127">-Name</span></span>
<span data-ttu-id="9cc81-128">A felügyelt Kubanetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="9cc81-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9cc81-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cc81-129">-PassThru</span></span>
<span data-ttu-id="9cc81-130">Eredménye igaz, ha az importálás sikeres</span><span class="sxs-lookup"><span data-stu-id="9cc81-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="9cc81-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cc81-131">-ResourceGroupName</span></span>
<span data-ttu-id="9cc81-132">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9cc81-132">Resource group name</span></span>

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

### <span data-ttu-id="9cc81-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cc81-133">-Confirm</span></span>
<span data-ttu-id="9cc81-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9cc81-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc81-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc81-135">-WhatIf</span></span>
<span data-ttu-id="9cc81-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9cc81-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cc81-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cc81-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc81-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc81-138">CommonParameters</span></span>
<span data-ttu-id="9cc81-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cc81-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc81-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cc81-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc81-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cc81-141">INPUTS</span></span>

### <span data-ttu-id="9cc81-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="9cc81-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="9cc81-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9cc81-143">System.String</span></span>

## <span data-ttu-id="9cc81-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cc81-144">OUTPUTS</span></span>

### <span data-ttu-id="9cc81-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9cc81-145">System.String</span></span>

## <span data-ttu-id="9cc81-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9cc81-146">NOTES</span></span>

## <span data-ttu-id="9cc81-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cc81-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187100"
---
# <span data-ttu-id="f3660-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="f3660-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="f3660-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3660-102">SYNOPSIS</span></span>
<span data-ttu-id="f3660-103">Hozzon létre egy Kubectl SSH-alagutat a felügyelt fürt irányítópultjának.</span><span class="sxs-lookup"><span data-stu-id="f3660-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="f3660-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3660-104">SYNTAX</span></span>

### <span data-ttu-id="f3660-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f3660-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3660-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3660-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3660-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3660-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3660-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3660-108">DESCRIPTION</span></span>
<span data-ttu-id="f3660-109">Hozzon létre egy Kubectl SSH-alagutat a felügyelt fürt irányítópultjának.</span><span class="sxs-lookup"><span data-stu-id="f3660-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="f3660-110">Az SSH bújtatási alagút egy Kubectl-Tunnel nevű PowerShell-feladatban van beállítva, és futtatásuk folyamatban van `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="f3660-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="f3660-111">Az alagútnak elérhetőnek kell lennie a kapcsolaton keresztül [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="f3660-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="f3660-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f3660-112">EXAMPLES</span></span>

### <span data-ttu-id="f3660-113">SSH-alagút indítása és böngésző megnyitása a Kubernetes-irányítópultra</span><span class="sxs-lookup"><span data-stu-id="f3660-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="f3660-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3660-114">PARAMETERS</span></span>

### <span data-ttu-id="f3660-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3660-115">-DefaultProfile</span></span>
<span data-ttu-id="f3660-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3660-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3660-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="f3660-117">-DisableBrowser</span></span>
<span data-ttu-id="f3660-118">Do not pop: nyisson meg egy böngészőt, miután létrehozta a kubectl-portot – előre.</span><span class="sxs-lookup"><span data-stu-id="f3660-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="f3660-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f3660-119">-Id</span></span>
<span data-ttu-id="f3660-120">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="f3660-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f3660-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3660-121">-InputObject</span></span>
<span data-ttu-id="f3660-122">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="f3660-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3660-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="f3660-123">-ListenPort</span></span>
<span data-ttu-id="f3660-124">Az irányítópult figyelési portja.</span><span class="sxs-lookup"><span data-stu-id="f3660-124">The listening port for the dashboard.</span></span> <span data-ttu-id="f3660-125">Az alapértelmezett érték a 8003.</span><span class="sxs-lookup"><span data-stu-id="f3660-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3660-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3660-126">-Name</span></span>
<span data-ttu-id="f3660-127">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="f3660-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f3660-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3660-128">-PassThru</span></span>
<span data-ttu-id="f3660-129">A parancsmag az átadott KubeTunnelJob adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f3660-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="f3660-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3660-130">-ResourceGroupName</span></span>
<span data-ttu-id="f3660-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f3660-131">Resource group name</span></span>

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

### <span data-ttu-id="f3660-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3660-132">CommonParameters</span></span>
<span data-ttu-id="f3660-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3660-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3660-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f3660-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3660-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3660-135">INPUTS</span></span>

### <span data-ttu-id="f3660-136">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f3660-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="f3660-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f3660-137">System.String</span></span>

## <span data-ttu-id="f3660-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3660-138">OUTPUTS</span></span>

### <span data-ttu-id="f3660-139">Microsoft. Azure. Command. AK. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="f3660-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="f3660-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3660-140">NOTES</span></span>

## <span data-ttu-id="f3660-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3660-141">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357095"
---
# <span data-ttu-id="c521d-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="c521d-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="c521d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c521d-102">SYNOPSIS</span></span>
<span data-ttu-id="c521d-103">Hozzon létre egy Kutectl SSH-csatornát a felügyelt fürt irányítópultjához.</span><span class="sxs-lookup"><span data-stu-id="c521d-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="c521d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c521d-104">SYNTAX</span></span>

### <span data-ttu-id="c521d-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c521d-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c521d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c521d-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c521d-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c521d-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c521d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c521d-108">DESCRIPTION</span></span>
<span data-ttu-id="c521d-109">Hozzon létre egy Kutectl SSH-csatornát a felügyelt fürt irányítópultjához.</span><span class="sxs-lookup"><span data-stu-id="c521d-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="c521d-110">Az SSH-csatornát egy PowerShellKubectl-Tunnel nevű feladatban lehet beállítani, amely futtatásával található `Get-Job` meg.</span><span class="sxs-lookup"><span data-stu-id="c521d-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="c521d-111">Az átjárónak elérhetőnek kell [http://127.0.0.1:8001](http://127.0.0.1:8001) lennie.</span><span class="sxs-lookup"><span data-stu-id="c521d-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="c521d-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c521d-112">EXAMPLES</span></span>

### <span data-ttu-id="c521d-113">SSH-csatornát indít, és megnyit egy böngészőt a Tallernetes irányítópultján</span><span class="sxs-lookup"><span data-stu-id="c521d-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="c521d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c521d-114">PARAMETERS</span></span>

### <span data-ttu-id="c521d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c521d-115">-DefaultProfile</span></span>
<span data-ttu-id="c521d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c521d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c521d-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="c521d-117">-DisableBrowser</span></span>
<span data-ttu-id="c521d-118">Ne nyissa meg a böngészőt a metectl port forward létrehozása után.</span><span class="sxs-lookup"><span data-stu-id="c521d-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="c521d-119">-Id</span><span class="sxs-lookup"><span data-stu-id="c521d-119">-Id</span></span>
<span data-ttu-id="c521d-120">Felügyelt Kubanetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="c521d-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c521d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c521d-121">-InputObject</span></span>
<span data-ttu-id="c521d-122">EGY PSKubernetesCluster-objektum, amely általában a folyamaton keresztül megy keresztül.</span><span class="sxs-lookup"><span data-stu-id="c521d-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c521d-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="c521d-123">-ListenPort</span></span>
<span data-ttu-id="c521d-124">Az irányítópult figyelási portja.</span><span class="sxs-lookup"><span data-stu-id="c521d-124">The listening port for the dashboard.</span></span> <span data-ttu-id="c521d-125">Az alapértelmezett érték 8003.</span><span class="sxs-lookup"><span data-stu-id="c521d-125">Default value is 8003.</span></span>

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

### <span data-ttu-id="c521d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c521d-126">-Name</span></span>
<span data-ttu-id="c521d-127">A felügyelt Kubanetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="c521d-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c521d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c521d-128">-PassThru</span></span>
<span data-ttu-id="c521d-129">A parancsmag visszaadja a KubeTunnel Parancsmagot, ha az érték meg van edzve.</span><span class="sxs-lookup"><span data-stu-id="c521d-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="c521d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c521d-130">-ResourceGroupName</span></span>
<span data-ttu-id="c521d-131">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c521d-131">Resource group name</span></span>

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

### <span data-ttu-id="c521d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c521d-132">CommonParameters</span></span>
<span data-ttu-id="c521d-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c521d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c521d-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c521d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c521d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c521d-135">INPUTS</span></span>

### <span data-ttu-id="c521d-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c521d-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c521d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c521d-137">System.String</span></span>

## <span data-ttu-id="c521d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c521d-138">OUTPUTS</span></span>

### <span data-ttu-id="c521d-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="c521d-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="c521d-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c521d-140">NOTES</span></span>

## <span data-ttu-id="c521d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c521d-141">RELATED LINKS</span></span>

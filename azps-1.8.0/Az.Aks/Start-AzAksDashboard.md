---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 74c5504196a96408d66f8d64391552ebbc4449c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665743"
---
# <span data-ttu-id="f0317-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="f0317-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="f0317-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0317-102">SYNOPSIS</span></span>
<span data-ttu-id="f0317-103">Hozzon létre egy Kubectl SSH-alagutat a felügyelt fürt irányítópultjának.</span><span class="sxs-lookup"><span data-stu-id="f0317-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="f0317-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0317-104">SYNTAX</span></span>

### <span data-ttu-id="f0317-105">GroupNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0317-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0317-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0317-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0317-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0317-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0317-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0317-108">DESCRIPTION</span></span>
<span data-ttu-id="f0317-109">Hozzon létre egy Kubectl SSH-alagutat a felügyelt fürt irányítópultjának.</span><span class="sxs-lookup"><span data-stu-id="f0317-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="f0317-110">Az SSH bújtatási alagút egy Kubectl-Tunnel nevű PowerShell-feladatban van beállítva, és futtatásuk folyamatban van `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="f0317-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="f0317-111">Az alagútnak keresztül elérhetőnek kell lennie [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="f0317-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="f0317-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f0317-112">EXAMPLES</span></span>

### <span data-ttu-id="f0317-113">SSH-alagút indítása és böngésző megnyitása a Kubernetes-irányítópultra</span><span class="sxs-lookup"><span data-stu-id="f0317-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="f0317-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0317-114">PARAMETERS</span></span>

### <span data-ttu-id="f0317-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0317-115">-DefaultProfile</span></span>
<span data-ttu-id="f0317-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0317-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0317-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="f0317-117">-DisableBrowser</span></span>
<span data-ttu-id="f0317-118">Do not pop: nyisson meg egy böngészőt, miután establising a kubectl portot – előre.</span><span class="sxs-lookup"><span data-stu-id="f0317-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

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

### <span data-ttu-id="f0317-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f0317-119">-Id</span></span>
<span data-ttu-id="f0317-120">Felügyelt Kubernetes-fürt azonosítója</span><span class="sxs-lookup"><span data-stu-id="f0317-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f0317-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0317-121">-InputObject</span></span>
<span data-ttu-id="f0317-122">Egy PSKubernetesCluster objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="f0317-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="f0317-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0317-123">-Name</span></span>
<span data-ttu-id="f0317-124">A felügyelt Kubernetes-fürt neve</span><span class="sxs-lookup"><span data-stu-id="f0317-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f0317-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0317-125">-PassThru</span></span>
<span data-ttu-id="f0317-126">A parancsmag az átadott KubeTunnelJob adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f0317-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="f0317-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0317-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0317-128">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f0317-128">Resource group name</span></span>

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

### <span data-ttu-id="f0317-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0317-129">CommonParameters</span></span>
<span data-ttu-id="f0317-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0317-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0317-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0317-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0317-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0317-132">INPUTS</span></span>

### <span data-ttu-id="f0317-133">Microsoft. Azure. Command. AK. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="f0317-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="f0317-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f0317-134">System.String</span></span>

## <span data-ttu-id="f0317-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0317-135">OUTPUTS</span></span>

### <span data-ttu-id="f0317-136">Microsoft. Azure. Command. AK. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="f0317-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="f0317-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0317-137">NOTES</span></span>

## <span data-ttu-id="f0317-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0317-138">RELATED LINKS</span></span>

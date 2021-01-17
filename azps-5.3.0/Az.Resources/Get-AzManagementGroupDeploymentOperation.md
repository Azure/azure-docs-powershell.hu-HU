---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466527"
---
# <span data-ttu-id="0cba3-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0cba3-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="0cba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cba3-102">SYNOPSIS</span></span>
<span data-ttu-id="0cba3-103">Telepítési művelet a felügyeleti csoportok központi telepítéséhez</span><span class="sxs-lookup"><span data-stu-id="0cba3-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="0cba3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0cba3-104">SYNTAX</span></span>

### <span data-ttu-id="0cba3-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0cba3-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cba3-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0cba3-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cba3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0cba3-107">DESCRIPTION</span></span>
<span data-ttu-id="0cba3-108">A **Get-AzManagementGroupDeploymentOperation parancsmag** felsorolja azokat a műveleteket, amelyek egy felügyeleti csoport központi telepítésében voltak, hogy segítsen azonosítani és további információt adni az adott telepítésben sikertelen műveletekről.</span><span class="sxs-lookup"><span data-stu-id="0cba3-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="0cba3-109">Ezek ugyanazok az információk, amelyek a portál telepítési részleteiben is megegyezik.</span><span class="sxs-lookup"><span data-stu-id="0cba3-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="0cba3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0cba3-110">EXAMPLES</span></span>

### <span data-ttu-id="0cba3-111">1. példa: Telepítési műveletek lekérte a telepítés nevét</span><span class="sxs-lookup"><span data-stu-id="0cba3-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="0cba3-112">Az "Deploy01" nevű telepítési műveleteket a "myMG" felügyeleti csoportban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0cba3-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="0cba3-113">2. példa: Telepítési és telepítési műveletek lekérte</span><span class="sxs-lookup"><span data-stu-id="0cba3-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="0cba3-114">Ez a parancs a "Deploy01" üzembe helyezést a "myMG" felügyeleti csoportban kapja meg, és beveszi a telepítési műveleteket.</span><span class="sxs-lookup"><span data-stu-id="0cba3-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="0cba3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cba3-115">PARAMETERS</span></span>

### <span data-ttu-id="0cba3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cba3-116">-DefaultProfile</span></span>
<span data-ttu-id="0cba3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cba3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cba3-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="0cba3-118">-DeploymentName</span></span>
<span data-ttu-id="0cba3-119">A telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="0cba3-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cba3-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0cba3-120">-DeploymentObject</span></span>
<span data-ttu-id="0cba3-121">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="0cba3-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cba3-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0cba3-122">-ManagementGroupId</span></span>
<span data-ttu-id="0cba3-123">A felügyeleti csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0cba3-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cba3-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0cba3-124">-OperationId</span></span>
<span data-ttu-id="0cba3-125">A telepítési művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0cba3-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cba3-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="0cba3-126">-Pre</span></span>
<span data-ttu-id="0cba3-127">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0cba3-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0cba3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cba3-128">CommonParameters</span></span>
<span data-ttu-id="0cba3-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cba3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cba3-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cba3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cba3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cba3-131">INPUTS</span></span>

### <span data-ttu-id="0cba3-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0cba3-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0cba3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cba3-133">OUTPUTS</span></span>

### <span data-ttu-id="0cba3-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0cba3-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="0cba3-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0cba3-135">NOTES</span></span>

## <span data-ttu-id="0cba3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cba3-136">RELATED LINKS</span></span>

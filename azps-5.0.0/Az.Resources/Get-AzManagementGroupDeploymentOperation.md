---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301172"
---
# <span data-ttu-id="ae2dc-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ae2dc-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="ae2dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae2dc-103">Üzembe állítási művelet beszerzése a felügyeleti csoport központi telepítéséhez</span><span class="sxs-lookup"><span data-stu-id="ae2dc-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="ae2dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae2dc-104">SYNTAX</span></span>

### <span data-ttu-id="ae2dc-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae2dc-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae2dc-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ae2dc-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae2dc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae2dc-107">DESCRIPTION</span></span>
<span data-ttu-id="ae2dc-108">A **Get-AzManagementGroupDeploymentOperation** parancsmag felsorolja azokat a műveleteket, amelyek a felügyeleti csoportba foglaltak, így könnyebben megtalálhatja és megadhatja az adott üzembe állítással kapcsolatos pontos műveletekkel kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="ae2dc-109">Ez a cikk a portálon található központi verzió központi telepítéséhez szükséges információkat ismerteti.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="ae2dc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ae2dc-110">EXAMPLES</span></span>

### <span data-ttu-id="ae2dc-111">1. példa: központi telepítői műveletek beszerzése a központi telepítő nevében</span><span class="sxs-lookup"><span data-stu-id="ae2dc-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="ae2dc-112">A "Deploy01" nevű "myMG" felügyeleti csoport "" nevű központi telepítését adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="ae2dc-113">2. példa: központi üzembe állítási műveletek beszerzése</span><span class="sxs-lookup"><span data-stu-id="ae2dc-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="ae2dc-114">Ez a parancs a "Deploy01" ("myMG") felügyeleti csoport "" üzembe állítását, valamint a központi üzembe állítási műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="ae2dc-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae2dc-115">PARAMETERS</span></span>

### <span data-ttu-id="ae2dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae2dc-116">-DefaultProfile</span></span>
<span data-ttu-id="ae2dc-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae2dc-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="ae2dc-118">-DeploymentName</span></span>
<span data-ttu-id="ae2dc-119">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-119">The deployment name.</span></span>

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

### <span data-ttu-id="ae2dc-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ae2dc-120">-DeploymentObject</span></span>
<span data-ttu-id="ae2dc-121">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-121">The deployment object.</span></span>

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

### <span data-ttu-id="ae2dc-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ae2dc-122">-ManagementGroupId</span></span>
<span data-ttu-id="ae2dc-123">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-123">The management group id.</span></span>

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

### <span data-ttu-id="ae2dc-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ae2dc-124">-OperationId</span></span>
<span data-ttu-id="ae2dc-125">A központi telepítő műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="ae2dc-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="ae2dc-126">-Pre</span></span>
<span data-ttu-id="ae2dc-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ae2dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae2dc-128">CommonParameters</span></span>
<span data-ttu-id="ae2dc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae2dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae2dc-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ae2dc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae2dc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae2dc-131">INPUTS</span></span>

### <span data-ttu-id="ae2dc-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ae2dc-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ae2dc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae2dc-133">OUTPUTS</span></span>

### <span data-ttu-id="ae2dc-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ae2dc-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="ae2dc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae2dc-135">NOTES</span></span>

## <span data-ttu-id="ae2dc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae2dc-136">RELATED LINKS</span></span>

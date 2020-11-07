---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846781"
---
# <span data-ttu-id="a3859-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3859-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="a3859-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3859-102">SYNOPSIS</span></span>
<span data-ttu-id="a3859-103">Üzembe állítási művelet beszerzése a felügyeleti csoport központi telepítéséhez</span><span class="sxs-lookup"><span data-stu-id="a3859-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="a3859-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3859-104">SYNTAX</span></span>

### <span data-ttu-id="a3859-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3859-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3859-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a3859-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3859-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3859-107">DESCRIPTION</span></span>
<span data-ttu-id="a3859-108">A **Get-AzManagementGroupDeploymentOperation** parancsmag felsorolja azokat a műveleteket, amelyek a felügyeleti csoportba foglaltak, így könnyebben megtalálhatja és megadhatja az adott üzembe állítással kapcsolatos pontos műveletekkel kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="a3859-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="a3859-109">Ez a cikk a portálon található központi verzió központi telepítéséhez szükséges információkat ismerteti.</span><span class="sxs-lookup"><span data-stu-id="a3859-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="a3859-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a3859-110">EXAMPLES</span></span>

### <span data-ttu-id="a3859-111">1. példa: központi telepítői műveletek beszerzése a központi telepítő nevében</span><span class="sxs-lookup"><span data-stu-id="a3859-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="a3859-112">A "Deploy01" nevű "myMG" felügyeleti csoport "" nevű központi telepítését adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3859-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="a3859-113">2. példa: központi üzembe állítási műveletek beszerzése</span><span class="sxs-lookup"><span data-stu-id="a3859-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="a3859-114">Ez a parancs a "Deploy01" ("myMG") felügyeleti csoport "" üzembe állítását, valamint a központi üzembe állítási műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a3859-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="a3859-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3859-115">PARAMETERS</span></span>

### <span data-ttu-id="a3859-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a3859-116">-ApiVersion</span></span>
<span data-ttu-id="a3859-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3859-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a3859-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a3859-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3859-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3859-119">-DefaultProfile</span></span>
<span data-ttu-id="a3859-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3859-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3859-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a3859-121">-DeploymentName</span></span>
<span data-ttu-id="a3859-122">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="a3859-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3859-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a3859-123">-DeploymentObject</span></span>
<span data-ttu-id="a3859-124">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="a3859-124">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3859-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a3859-125">-ManagementGroupId</span></span>
<span data-ttu-id="a3859-126">A kezelési csoport azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3859-126">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3859-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a3859-127">-OperationId</span></span>
<span data-ttu-id="a3859-128">A központi telepítő műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="a3859-128">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3859-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="a3859-129">-Pre</span></span>
<span data-ttu-id="a3859-130">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a3859-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a3859-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3859-131">CommonParameters</span></span>
<span data-ttu-id="a3859-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3859-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3859-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3859-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3859-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3859-134">INPUTS</span></span>

### <span data-ttu-id="a3859-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a3859-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a3859-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3859-136">OUTPUTS</span></span>

### <span data-ttu-id="a3859-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3859-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="a3859-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3859-138">NOTES</span></span>

## <span data-ttu-id="a3859-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3859-139">RELATED LINKS</span></span>

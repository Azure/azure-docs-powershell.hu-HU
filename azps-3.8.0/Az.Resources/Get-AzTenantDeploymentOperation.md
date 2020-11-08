---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: 4505a64b25f0022763541e6cd5d700e7c6c05988
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013777"
---
# <span data-ttu-id="7673c-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7673c-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="7673c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7673c-102">SYNOPSIS</span></span>
<span data-ttu-id="7673c-103">Üzembe állítási művelet beszerzése a bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="7673c-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="7673c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7673c-104">SYNTAX</span></span>

### <span data-ttu-id="7673c-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7673c-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7673c-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7673c-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7673c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7673c-107">DESCRIPTION</span></span>
<span data-ttu-id="7673c-108">A **Get-AzTenantDeploymentOperation** parancsmag felsorolja azokat a műveleteket, amelyek a jelenlegi bérlői hatókörben a központi üzembe állítás része volt, így könnyebben megtalálhatja és megadhatja az adott üzembe állítás hibáinak pontos műveleteit.</span><span class="sxs-lookup"><span data-stu-id="7673c-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="7673c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7673c-109">EXAMPLES</span></span>

### <span data-ttu-id="7673c-110">1. példa: központi telepítői műveletek beszerzése a központi telepítő nevében</span><span class="sxs-lookup"><span data-stu-id="7673c-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="7673c-111">A "Deploy01" nevű "bevezetési műveletek" kifejezés a jelenlegi bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="7673c-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="7673c-112">2. példa: központi üzembe állítási műveletek beszerzése</span><span class="sxs-lookup"><span data-stu-id="7673c-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="7673c-113">A parancs a jelenlegi bérlői hatókörben a "Deploy01" bevezetést kapja, és üzembe állítási műveleteit kapja.</span><span class="sxs-lookup"><span data-stu-id="7673c-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="7673c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7673c-114">PARAMETERS</span></span>

### <span data-ttu-id="7673c-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7673c-115">-ApiVersion</span></span>
<span data-ttu-id="7673c-116">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7673c-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7673c-117">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7673c-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7673c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7673c-118">-DefaultProfile</span></span>
<span data-ttu-id="7673c-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7673c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7673c-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="7673c-120">-DeploymentName</span></span>
<span data-ttu-id="7673c-121">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="7673c-121">The deployment name.</span></span>

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

### <span data-ttu-id="7673c-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7673c-122">-DeploymentObject</span></span>
<span data-ttu-id="7673c-123">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="7673c-123">The deployment object.</span></span>

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

### <span data-ttu-id="7673c-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7673c-124">-OperationId</span></span>
<span data-ttu-id="7673c-125">A központi telepítő műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="7673c-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="7673c-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="7673c-126">-Pre</span></span>
<span data-ttu-id="7673c-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7673c-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7673c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7673c-128">CommonParameters</span></span>
<span data-ttu-id="7673c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7673c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7673c-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7673c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7673c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7673c-131">INPUTS</span></span>

### <span data-ttu-id="7673c-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7673c-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7673c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7673c-133">OUTPUTS</span></span>

### <span data-ttu-id="7673c-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7673c-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="7673c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7673c-135">NOTES</span></span>

## <span data-ttu-id="7673c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7673c-136">RELATED LINKS</span></span>

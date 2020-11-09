---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301061"
---
# <span data-ttu-id="1b57d-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1b57d-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="1b57d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b57d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b57d-103">Üzembe állítási művelet beszerzése a bérlői hatókörben</span><span class="sxs-lookup"><span data-stu-id="1b57d-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="1b57d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b57d-104">SYNTAX</span></span>

### <span data-ttu-id="1b57d-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b57d-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b57d-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1b57d-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b57d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b57d-107">DESCRIPTION</span></span>
<span data-ttu-id="1b57d-108">A **Get-AzTenantDeploymentOperation** parancsmag felsorolja azokat a műveleteket, amelyek a jelenlegi bérlői hatókörben a központi üzembe állítás része volt, így könnyebben megtalálhatja és megadhatja az adott üzembe állítás hibáinak pontos műveleteit.</span><span class="sxs-lookup"><span data-stu-id="1b57d-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="1b57d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1b57d-109">EXAMPLES</span></span>

### <span data-ttu-id="1b57d-110">1. példa: központi telepítői műveletek beszerzése a központi telepítő nevében</span><span class="sxs-lookup"><span data-stu-id="1b57d-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="1b57d-111">A "Deploy01" nevű "bevezetési műveletek" kifejezés a jelenlegi bérlői hatókörben.</span><span class="sxs-lookup"><span data-stu-id="1b57d-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="1b57d-112">2. példa: központi üzembe állítási műveletek beszerzése</span><span class="sxs-lookup"><span data-stu-id="1b57d-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="1b57d-113">A parancs a jelenlegi bérlői hatókörben a "Deploy01" bevezetést kapja, és üzembe állítási műveleteit kapja.</span><span class="sxs-lookup"><span data-stu-id="1b57d-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="1b57d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b57d-114">PARAMETERS</span></span>

### <span data-ttu-id="1b57d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b57d-115">-DefaultProfile</span></span>
<span data-ttu-id="1b57d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b57d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b57d-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="1b57d-117">-DeploymentName</span></span>
<span data-ttu-id="1b57d-118">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="1b57d-118">The deployment name.</span></span>

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

### <span data-ttu-id="1b57d-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1b57d-119">-DeploymentObject</span></span>
<span data-ttu-id="1b57d-120">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="1b57d-120">The deployment object.</span></span>

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

### <span data-ttu-id="1b57d-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1b57d-121">-OperationId</span></span>
<span data-ttu-id="1b57d-122">A központi telepítő műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="1b57d-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="1b57d-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="1b57d-123">-Pre</span></span>
<span data-ttu-id="1b57d-124">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="1b57d-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1b57d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b57d-125">CommonParameters</span></span>
<span data-ttu-id="1b57d-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b57d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b57d-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1b57d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b57d-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b57d-128">INPUTS</span></span>

### <span data-ttu-id="1b57d-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1b57d-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1b57d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b57d-130">OUTPUTS</span></span>

### <span data-ttu-id="1b57d-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1b57d-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="1b57d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b57d-132">NOTES</span></span>

## <span data-ttu-id="1b57d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b57d-133">RELATED LINKS</span></span>

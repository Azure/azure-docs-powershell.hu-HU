---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466488"
---
# <span data-ttu-id="fddeb-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="fddeb-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="fddeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fddeb-102">SYNOPSIS</span></span>
<span data-ttu-id="fddeb-103">Telepítési művelet lekérte a bérlői webhely hatókörében való üzembe helyezést</span><span class="sxs-lookup"><span data-stu-id="fddeb-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="fddeb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fddeb-104">SYNTAX</span></span>

### <span data-ttu-id="fddeb-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fddeb-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fddeb-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="fddeb-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fddeb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fddeb-107">DESCRIPTION</span></span>
<span data-ttu-id="fddeb-108">A **Get-AztenantDeploymentOperation parancsmag** felsorolja azokat a műveleteket, amelyek a jelenlegi bérlői tartományba való telepítés részét képezték, hogy ön azonosítsa és további információt nyújtson az adott központi telepítés pontos műveleteiről.</span><span class="sxs-lookup"><span data-stu-id="fddeb-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="fddeb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fddeb-109">EXAMPLES</span></span>

### <span data-ttu-id="fddeb-110">1. példa: Telepítési műveletek lekérte a telepítés nevét</span><span class="sxs-lookup"><span data-stu-id="fddeb-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="fddeb-111">Az aktuális bérlői hatókörben a "Deploy01" nevű telepítési műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fddeb-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="fddeb-112">2. példa: Telepítési és telepítési műveletek lekérte</span><span class="sxs-lookup"><span data-stu-id="fddeb-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="fddeb-113">Ez a parancs a központi telepítés "Deploy01" (Üzembe helyezés) parancsát a bérlő aktuális hatókörében kapja meg, és beveszi a telepítési műveleteket.</span><span class="sxs-lookup"><span data-stu-id="fddeb-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="fddeb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fddeb-114">PARAMETERS</span></span>

### <span data-ttu-id="fddeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddeb-115">-DefaultProfile</span></span>
<span data-ttu-id="fddeb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fddeb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fddeb-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="fddeb-117">-DeploymentName</span></span>
<span data-ttu-id="fddeb-118">A telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="fddeb-118">The deployment name.</span></span>

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

### <span data-ttu-id="fddeb-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="fddeb-119">-DeploymentObject</span></span>
<span data-ttu-id="fddeb-120">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="fddeb-120">The deployment object.</span></span>

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

### <span data-ttu-id="fddeb-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fddeb-121">-OperationId</span></span>
<span data-ttu-id="fddeb-122">A telepítési művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fddeb-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="fddeb-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="fddeb-123">-Pre</span></span>
<span data-ttu-id="fddeb-124">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="fddeb-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fddeb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddeb-125">CommonParameters</span></span>
<span data-ttu-id="fddeb-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fddeb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddeb-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fddeb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddeb-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fddeb-128">INPUTS</span></span>

### <span data-ttu-id="fddeb-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="fddeb-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="fddeb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fddeb-130">OUTPUTS</span></span>

### <span data-ttu-id="fddeb-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="fddeb-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="fddeb-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fddeb-132">NOTES</span></span>

## <span data-ttu-id="fddeb-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fddeb-133">RELATED LINKS</span></span>

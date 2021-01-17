---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466544"
---
# <span data-ttu-id="16884-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="16884-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="16884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16884-102">SYNOPSIS</span></span>
<span data-ttu-id="16884-103">Telepítési művelet</span><span class="sxs-lookup"><span data-stu-id="16884-103">Get deployment operation</span></span>

## <span data-ttu-id="16884-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="16884-104">SYNTAX</span></span>

### <span data-ttu-id="16884-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16884-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16884-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="16884-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16884-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="16884-107">DESCRIPTION</span></span>
<span data-ttu-id="16884-108">A **Get-AzDeploymentOperation** parancsmag felsorolja azokat a műveleteket, amelyek egy központi telepítés részét képezték, hogy ön azonosítsa és további információt nyújtson az adott telepítésben sikertelen műveletekről.</span><span class="sxs-lookup"><span data-stu-id="16884-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="16884-109">Emellett az egyes telepítési műveletek válaszát és kérési tartalmát is meg tudja mutatni.</span><span class="sxs-lookup"><span data-stu-id="16884-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="16884-110">Ezek ugyanazok az információk, amelyek a portál telepítési részleteiben is megegyezik.</span><span class="sxs-lookup"><span data-stu-id="16884-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="16884-111">A kérés és a választartalom lekéréséhez engedélyezze a beállítást, amikor a **New-AzDeployment** szolgáltatáson keresztül beküld egy központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="16884-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="16884-112">Naplózhat és felfedhet olyan titkosságokat, például az erőforrástulajdonságban vagy a **listKeys** műveletben használt jelszavakat, amelyek az üzembe helyezési műveletek lekérésekor ad vissza.</span><span class="sxs-lookup"><span data-stu-id="16884-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="16884-113">A beállításról és annak engedélyezéséről további információt a New-AzDeployment és ARM sablontelepítések</span><span class="sxs-lookup"><span data-stu-id="16884-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="16884-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="16884-114">EXAMPLES</span></span>

### <span data-ttu-id="16884-115">1. példa: Telepítési műveletek lekérte a telepítés nevét</span><span class="sxs-lookup"><span data-stu-id="16884-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="16884-116">Az aktuális előfizetési hatókörű "teszt" névvel üzembe helyezési műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="16884-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="16884-117">2. példa: Telepítési és telepítési műveletek lekérte</span><span class="sxs-lookup"><span data-stu-id="16884-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="16884-118">Ez a parancs a központi telepítés "tesztelését" kapja meg az aktuális előfizetés hatókörében, és be is szerezze a telepítési műveleteket.</span><span class="sxs-lookup"><span data-stu-id="16884-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="16884-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16884-119">PARAMETERS</span></span>

### <span data-ttu-id="16884-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16884-120">-DefaultProfile</span></span>
<span data-ttu-id="16884-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16884-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16884-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="16884-122">-DeploymentName</span></span>
<span data-ttu-id="16884-123">A telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="16884-123">The deployment name.</span></span>

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

### <span data-ttu-id="16884-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="16884-124">-DeploymentObject</span></span>
<span data-ttu-id="16884-125">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="16884-125">The deployment object.</span></span>

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

### <span data-ttu-id="16884-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="16884-126">-OperationId</span></span>
<span data-ttu-id="16884-127">A telepítési művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="16884-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="16884-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="16884-128">-Pre</span></span>
<span data-ttu-id="16884-129">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="16884-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="16884-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16884-130">CommonParameters</span></span>
<span data-ttu-id="16884-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16884-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16884-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16884-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16884-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16884-133">INPUTS</span></span>

### <span data-ttu-id="16884-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="16884-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="16884-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16884-135">OUTPUTS</span></span>

### <span data-ttu-id="16884-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="16884-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="16884-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="16884-137">NOTES</span></span>

## <span data-ttu-id="16884-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16884-138">RELATED LINKS</span></span>

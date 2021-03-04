---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 5507e180d5f56b75006f31f9cc6753f50d821a3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929418"
---
# <span data-ttu-id="4d7af-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="4d7af-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="4d7af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d7af-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7af-103">Telepítési művelet</span><span class="sxs-lookup"><span data-stu-id="4d7af-103">Get deployment operation</span></span>

## <span data-ttu-id="4d7af-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d7af-104">SYNTAX</span></span>

### <span data-ttu-id="4d7af-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d7af-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d7af-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4d7af-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d7af-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d7af-107">DESCRIPTION</span></span>
<span data-ttu-id="4d7af-108">A **Get-AzDeploymentOperation** parancsmag felsorolja az összes olyan műveletet, amely egy telepítés része volt, hogy segítsen azonosítani és további információt adni az adott telepítésben sikertelen műveletekről.</span><span class="sxs-lookup"><span data-stu-id="4d7af-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="4d7af-109">Emellett az egyes telepítési műveletek válaszát és kérési tartalmát is meg tudja mutatni.</span><span class="sxs-lookup"><span data-stu-id="4d7af-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="4d7af-110">Ezek ugyanazok az információk, amelyek a portál telepítési részleteiben is megegyezik.</span><span class="sxs-lookup"><span data-stu-id="4d7af-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="4d7af-111">A kérés és a választartalom lekéréséhez engedélyezze a beállítást, amikor a **New-AzDeployment** szolgáltatáson keresztül beküld egy központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="4d7af-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="4d7af-112">Naplózhat és felfedhet olyan titkosságokat, például az erőforrástulajdonságban vagy a **listKeys** műveletben használt jelszavakat, amelyek az üzembe helyezési műveletek lekérésekor ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4d7af-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="4d7af-113">A beállításról és annak engedélyezéséről további információt a New-AzDeployment és ARM sablontelepítések</span><span class="sxs-lookup"><span data-stu-id="4d7af-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="4d7af-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d7af-114">EXAMPLES</span></span>

### <span data-ttu-id="4d7af-115">1. példa: Telepítési műveletek lekérte a telepítés nevét</span><span class="sxs-lookup"><span data-stu-id="4d7af-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="4d7af-116">Az aktuális előfizetési hatókörű "teszt" névvel üzembe helyezési műveletet kap.</span><span class="sxs-lookup"><span data-stu-id="4d7af-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="4d7af-117">2. példa: Telepítési és telepítési műveletek lekérte</span><span class="sxs-lookup"><span data-stu-id="4d7af-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="4d7af-118">Ez a parancs a központi telepítés "tesztelését" kapja meg az aktuális előfizetés hatókörében, és be is szerezze a telepítési műveleteket.</span><span class="sxs-lookup"><span data-stu-id="4d7af-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="4d7af-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d7af-119">PARAMETERS</span></span>

### <span data-ttu-id="4d7af-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7af-120">-DefaultProfile</span></span>
<span data-ttu-id="4d7af-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d7af-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d7af-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4d7af-122">-DeploymentName</span></span>
<span data-ttu-id="4d7af-123">A telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="4d7af-123">The deployment name.</span></span>

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

### <span data-ttu-id="4d7af-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4d7af-124">-DeploymentObject</span></span>
<span data-ttu-id="4d7af-125">A telepítőobjektum.</span><span class="sxs-lookup"><span data-stu-id="4d7af-125">The deployment object.</span></span>

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

### <span data-ttu-id="4d7af-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4d7af-126">-OperationId</span></span>
<span data-ttu-id="4d7af-127">A telepítési művelet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4d7af-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="4d7af-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="4d7af-128">-Pre</span></span>
<span data-ttu-id="4d7af-129">Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="4d7af-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4d7af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7af-130">CommonParameters</span></span>
<span data-ttu-id="4d7af-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d7af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7af-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d7af-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7af-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d7af-133">INPUTS</span></span>

### <span data-ttu-id="4d7af-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4d7af-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4d7af-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d7af-135">OUTPUTS</span></span>

### <span data-ttu-id="4d7af-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="4d7af-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="4d7af-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d7af-137">NOTES</span></span>

## <span data-ttu-id="4d7af-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d7af-138">RELATED LINKS</span></span>

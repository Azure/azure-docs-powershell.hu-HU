---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 809e7e82948d155ad73a80cbd430499d5372b644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838176"
---
# <span data-ttu-id="a6ae4-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a6ae4-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="a6ae4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ae4-103">Üzembe állítási művelet</span><span class="sxs-lookup"><span data-stu-id="a6ae4-103">Get deployment operation</span></span>

## <span data-ttu-id="a6ae4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6ae4-104">SYNTAX</span></span>

### <span data-ttu-id="a6ae4-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a6ae4-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6ae4-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a6ae4-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6ae4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6ae4-107">DESCRIPTION</span></span>
<span data-ttu-id="a6ae4-108">A **Get-AzDeploymentOperation** parancsmag a központi üzembe állítás részét képező összes műveletet felsorolja, így könnyebben megtalálhatja és megadhatja az adott üzembe állítással kapcsolatos pontos műveleteket.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="a6ae4-109">A válasz és a kérés tartalma is megjeleníthető az egyes üzembe állítási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="a6ae4-110">Ez a cikk a portálon található központi verzió központi telepítéséhez szükséges információkat ismerteti.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="a6ae4-111">A kérelem és a válasz tartalmának beszerzéséhez engedélyezze a beállítást, ha a bevezetést az **új AzDeployment-** on keresztül küldi el.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="a6ae4-112">Előfordulhat, hogy az erőforrás-tulajdonságokban vagy a **listKeys** -műveletekben használt jelszavakat, például a központi telepítési műveletek lekérése után visszaadott jelszavakat is naplózhatja és megjelenítheti.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="a6ae4-113">A beállításról és annak engedélyezéséről további információt a ARM-sablonok bevezetésének New-AzDeployment és hibakeresése című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="a6ae4-114">Példák</span><span class="sxs-lookup"><span data-stu-id="a6ae4-114">EXAMPLES</span></span>

### <span data-ttu-id="a6ae4-115">Központi telepítői műveletek beszerzése a központi telepítő nevében</span><span class="sxs-lookup"><span data-stu-id="a6ae4-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="a6ae4-116">A "teszt" nevű központi üzembe állítási művelet a jelenlegi előfizetési tartományban</span><span class="sxs-lookup"><span data-stu-id="a6ae4-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="a6ae4-117">Üzembe állítási műveletek beszerzése és üzembe állítása</span><span class="sxs-lookup"><span data-stu-id="a6ae4-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="a6ae4-118">Ez a parancs beilleszti a "teszt" műveletet a jelenlegi előfizetési tartományba, és beilleszti a központi üzembe állítási műveleteket.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="a6ae4-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6ae4-119">PARAMETERS</span></span>

### <span data-ttu-id="a6ae4-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a6ae4-120">-ApiVersion</span></span>
<span data-ttu-id="a6ae4-121">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a6ae4-122">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ae4-123">-DefaultProfile</span></span>
<span data-ttu-id="a6ae4-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6ae4-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a6ae4-125">-DeploymentName</span></span>
<span data-ttu-id="a6ae4-126">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-126">The deployment name.</span></span>

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

### <span data-ttu-id="a6ae4-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a6ae4-127">-DeploymentObject</span></span>
<span data-ttu-id="a6ae4-128">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-128">The deployment object.</span></span>

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

### <span data-ttu-id="a6ae4-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a6ae4-129">-OperationId</span></span>
<span data-ttu-id="a6ae4-130">A központi telepítő műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-130">The deployment operation Id.</span></span>

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

### <span data-ttu-id="a6ae4-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="a6ae4-131">-Pre</span></span>
<span data-ttu-id="a6ae4-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="a6ae4-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a6ae4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ae4-133">CommonParameters</span></span>
<span data-ttu-id="a6ae4-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6ae4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ae4-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ae4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ae4-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6ae4-136">INPUTS</span></span>

### <span data-ttu-id="a6ae4-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a6ae4-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a6ae4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6ae4-138">OUTPUTS</span></span>

### <span data-ttu-id="a6ae4-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a6ae4-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="a6ae4-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6ae4-140">NOTES</span></span>

## <span data-ttu-id="a6ae4-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6ae4-141">RELATED LINKS</span></span>

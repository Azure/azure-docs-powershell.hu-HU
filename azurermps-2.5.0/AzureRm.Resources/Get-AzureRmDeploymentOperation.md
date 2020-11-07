---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeploymentoperation
schema: 2.0.0
ms.openlocfilehash: 2bb5c3823d974dad53045d9283099befd4d60855
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850570"
---
# <span data-ttu-id="49a1a-101">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="49a1a-101">Get-AzureRmDeploymentOperation</span></span>

## <span data-ttu-id="49a1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="49a1a-103">Üzembe állítási művelet</span><span class="sxs-lookup"><span data-stu-id="49a1a-103">Get deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49a1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49a1a-104">SYNTAX</span></span>

### <span data-ttu-id="49a1a-105">GetByDeploymentName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49a1a-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49a1a-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="49a1a-106">GetByDeploymentObject</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49a1a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="49a1a-107">DESCRIPTION</span></span>
<span data-ttu-id="49a1a-108">A **Get-AzureRmDeploymentOperation** parancsmag a központi üzembe állítás részét képező összes műveletet felsorolja, így könnyebben megtalálhatja és megadhatja az adott üzembe állítással kapcsolatos pontos műveleteket.</span><span class="sxs-lookup"><span data-stu-id="49a1a-108">The **Get-AzureRmDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="49a1a-109">A válasz és a kérés tartalma is megjeleníthető az egyes üzembe állítási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="49a1a-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="49a1a-110">Ez a cikk a portálon található központi verzió központi telepítéséhez szükséges információkat ismerteti.</span><span class="sxs-lookup"><span data-stu-id="49a1a-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="49a1a-111">A kérelem és a válasz tartalmának beszerzéséhez engedélyezze a beállítást, ha a bevezetést az **új AzureRmDeployment-** on keresztül küldi el.</span><span class="sxs-lookup"><span data-stu-id="49a1a-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmDeployment**.</span></span>
<span data-ttu-id="49a1a-112">Előfordulhat, hogy az erőforrás-tulajdonságokban vagy a **listKeys** -műveletekben használt jelszavakat, például a központi telepítési műveletek lekérése után visszaadott jelszavakat is naplózhatja és megjelenítheti.</span><span class="sxs-lookup"><span data-stu-id="49a1a-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="49a1a-113">A beállításról és annak engedélyezéséről további információt a ARM-sablonok bevezetésének New-AzureRmDeployment és hibakeresése című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="49a1a-113">For more on this setting and how to enable it, see New-AzureRmDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="49a1a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="49a1a-114">EXAMPLES</span></span>

### <span data-ttu-id="49a1a-115">Központi telepítői műveletek beszerzése a központi telepítő nevében</span><span class="sxs-lookup"><span data-stu-id="49a1a-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzureRmDeploymentOperation -DeploymentName test
```

<span data-ttu-id="49a1a-116">A "teszt" nevű központi üzembe állítási művelet a jelenlegi előfizetési tartományban</span><span class="sxs-lookup"><span data-stu-id="49a1a-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="49a1a-117">Üzembe állítási műveletek beszerzése és üzembe állítása</span><span class="sxs-lookup"><span data-stu-id="49a1a-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "test" | Get-AzureRmDeploymentOperation
```

<span data-ttu-id="49a1a-118">Ez a parancs beilleszti a "teszt" műveletet a jelenlegi előfizetési tartományba, és beilleszti a központi üzembe állítási műveleteket.</span><span class="sxs-lookup"><span data-stu-id="49a1a-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="49a1a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49a1a-119">PARAMETERS</span></span>

### <span data-ttu-id="49a1a-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="49a1a-120">-ApiVersion</span></span>
<span data-ttu-id="49a1a-121">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="49a1a-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="49a1a-122">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="49a1a-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="49a1a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a1a-123">-DefaultProfile</span></span>
<span data-ttu-id="49a1a-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49a1a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a1a-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="49a1a-125">-DeploymentName</span></span>
<span data-ttu-id="49a1a-126">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="49a1a-126">The deployment name.</span></span>

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

### <span data-ttu-id="49a1a-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="49a1a-127">-DeploymentObject</span></span>
<span data-ttu-id="49a1a-128">A központi telepítő objektum.</span><span class="sxs-lookup"><span data-stu-id="49a1a-128">The deployment object.</span></span>

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

### <span data-ttu-id="49a1a-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="49a1a-129">-OperationId</span></span>
<span data-ttu-id="49a1a-130">A központi telepítő műveleti azonosító.</span><span class="sxs-lookup"><span data-stu-id="49a1a-130">The deployment operation Id.</span></span>

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

### <span data-ttu-id="49a1a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="49a1a-131">-Pre</span></span>
<span data-ttu-id="49a1a-132">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="49a1a-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="49a1a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a1a-133">CommonParameters</span></span>
<span data-ttu-id="49a1a-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49a1a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a1a-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a1a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a1a-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a1a-136">INPUTS</span></span>

### <span data-ttu-id="49a1a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="49a1a-137">System.String</span></span>
<span data-ttu-id="49a1a-138">System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="49a1a-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="49a1a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49a1a-139">OUTPUTS</span></span>

### <span data-ttu-id="49a1a-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="49a1a-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="49a1a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49a1a-141">NOTES</span></span>

## <span data-ttu-id="49a1a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49a1a-142">RELATED LINKS</span></span>

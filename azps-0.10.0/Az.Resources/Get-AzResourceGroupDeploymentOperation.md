---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 22438110dd66fbbb89e992d79f37b1e8e2e325d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843405"
---
# <span data-ttu-id="0969e-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0969e-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="0969e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0969e-102">SYNOPSIS</span></span>
<span data-ttu-id="0969e-103">Az erőforráscsoport-telepítő művelet beolvasása</span><span class="sxs-lookup"><span data-stu-id="0969e-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="0969e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0969e-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0969e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0969e-105">DESCRIPTION</span></span>
<span data-ttu-id="0969e-106">A **Get-AzResourceGroupDeploymentOperation** parancsmag a központi üzembe állítás részét képező összes műveletet felsorolja, így könnyebben megtalálhatja és megadhatja az adott üzembe állítással kapcsolatos pontos műveleteket.</span><span class="sxs-lookup"><span data-stu-id="0969e-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="0969e-107">A válasz és a kérés tartalma is megjeleníthető az egyes üzembe állítási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="0969e-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="0969e-108">Ez a cikk a portálon található központi verzió központi telepítéséhez szükséges információkat ismerteti.</span><span class="sxs-lookup"><span data-stu-id="0969e-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="0969e-109">A kérelem és a válasz tartalmának beszerzéséhez engedélyezze a beállítást, ha a bevezetést az **új AzResourceGroupDeployment-** on keresztül küldi el.</span><span class="sxs-lookup"><span data-stu-id="0969e-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="0969e-110">Előfordulhat, hogy az erőforrás-tulajdonságokban vagy a **listKeys** -műveletekben használt jelszavakat, például a központi telepítési műveletek lekérése után visszaadott jelszavakat is naplózhatja és megjelenítheti.</span><span class="sxs-lookup"><span data-stu-id="0969e-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="0969e-111">A beállításról és annak engedélyezéséről további információt a ARM-sablonok bevezetésének New-AzResourceGroupDeployment és hibakeresése című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0969e-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="0969e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0969e-112">EXAMPLES</span></span>

### <span data-ttu-id="0969e-113">Get1</span><span class="sxs-lookup"><span data-stu-id="0969e-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="0969e-114">A "teszt" nevű erőforráscsoport "teszt" nevű "teszt" nevű központi üzembe állítási művelete</span><span class="sxs-lookup"><span data-stu-id="0969e-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="0969e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0969e-115">PARAMETERS</span></span>

### <span data-ttu-id="0969e-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0969e-116">-ApiVersion</span></span>
<span data-ttu-id="0969e-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0969e-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0969e-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0969e-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0969e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0969e-119">-DefaultProfile</span></span>
<span data-ttu-id="0969e-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0969e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0969e-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="0969e-121">-DeploymentName</span></span>
<span data-ttu-id="0969e-122">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="0969e-122">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0969e-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0969e-123">-InformationAction</span></span>
<span data-ttu-id="0969e-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="0969e-124">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0969e-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0969e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0969e-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="0969e-126">Continue</span></span>
- <span data-ttu-id="0969e-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="0969e-127">Ignore</span></span>
- <span data-ttu-id="0969e-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="0969e-128">Inquire</span></span>
- <span data-ttu-id="0969e-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0969e-129">SilentlyContinue</span></span>
- <span data-ttu-id="0969e-130">állj</span><span class="sxs-lookup"><span data-stu-id="0969e-130">Stop</span></span>
- <span data-ttu-id="0969e-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="0969e-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0969e-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0969e-132">-InformationVariable</span></span>
<span data-ttu-id="0969e-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0969e-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0969e-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="0969e-134">-Pre</span></span>
<span data-ttu-id="0969e-135">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="0969e-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0969e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0969e-136">-ResourceGroupName</span></span>
<span data-ttu-id="0969e-137">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0969e-137">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0969e-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0969e-138">-SubscriptionId</span></span>
<span data-ttu-id="0969e-139">A használandó előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0969e-139">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0969e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0969e-140">CommonParameters</span></span>
<span data-ttu-id="0969e-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0969e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0969e-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0969e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0969e-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0969e-143">INPUTS</span></span>

## <span data-ttu-id="0969e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0969e-144">OUTPUTS</span></span>

## <span data-ttu-id="0969e-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0969e-145">NOTES</span></span>

## <span data-ttu-id="0969e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0969e-146">RELATED LINKS</span></span>

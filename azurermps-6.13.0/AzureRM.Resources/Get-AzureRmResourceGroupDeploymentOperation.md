---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 145c71001fa0812681ab3975fccbb0167de5d978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494954"
---
# <span data-ttu-id="7a9cd-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a9cd-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="7a9cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9cd-103">Az erőforráscsoport-telepítő művelet beolvasása</span><span class="sxs-lookup"><span data-stu-id="7a9cd-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a9cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a9cd-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7a9cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a9cd-105">DESCRIPTION</span></span>
<span data-ttu-id="7a9cd-106">A **Get-AzureRmResourceGroupDeploymentOperation** parancsmag a központi üzembe állítás részét képező összes műveletet felsorolja, így könnyebben megtalálhatja és megadhatja az adott üzembe állítással kapcsolatos pontos műveleteket.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="7a9cd-107">A válasz és a kérés tartalma is megjeleníthető az egyes üzembe állítási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="7a9cd-108">Ez a cikk a portálon található központi verzió központi telepítéséhez szükséges információkat ismerteti.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="7a9cd-109">A kérelem és a válasz tartalmának beszerzéséhez engedélyezze a beállítást, ha a bevezetést az **új AzureRmResourceGroupDeployment-** on keresztül küldi el.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="7a9cd-110">Előfordulhat, hogy az erőforrás-tulajdonságokban vagy a **listKeys** -műveletekben használt jelszavakat, például a központi telepítési műveletek lekérése után visszaadott jelszavakat is naplózhatja és megjelenítheti.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="7a9cd-111">A beállításról és annak engedélyezéséről további információt a ARM-sablonok bevezetésének New-AzureRmResourceGroupDeployment és hibakeresése című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="7a9cd-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7a9cd-112">EXAMPLES</span></span>

### <span data-ttu-id="7a9cd-113">Get1</span><span class="sxs-lookup"><span data-stu-id="7a9cd-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="7a9cd-114">A "teszt" nevű erőforráscsoport "teszt" nevű "teszt" nevű központi üzembe állítási művelete</span><span class="sxs-lookup"><span data-stu-id="7a9cd-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="7a9cd-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a9cd-115">PARAMETERS</span></span>

### <span data-ttu-id="7a9cd-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7a9cd-116">-ApiVersion</span></span>
<span data-ttu-id="7a9cd-117">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7a9cd-118">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7a9cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9cd-119">-DefaultProfile</span></span>
<span data-ttu-id="7a9cd-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7a9cd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a9cd-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="7a9cd-121">-DeploymentName</span></span>
<span data-ttu-id="7a9cd-122">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-122">The deployment name.</span></span>

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

### <span data-ttu-id="7a9cd-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7a9cd-123">-InformationAction</span></span>
<span data-ttu-id="7a9cd-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-124">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="7a9cd-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7a9cd-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7a9cd-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="7a9cd-126">Continue</span></span>
- <span data-ttu-id="7a9cd-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="7a9cd-127">Ignore</span></span>
- <span data-ttu-id="7a9cd-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="7a9cd-128">Inquire</span></span>
- <span data-ttu-id="7a9cd-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7a9cd-129">SilentlyContinue</span></span>
- <span data-ttu-id="7a9cd-130">állj</span><span class="sxs-lookup"><span data-stu-id="7a9cd-130">Stop</span></span>
- <span data-ttu-id="7a9cd-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="7a9cd-131">Suspend</span></span>

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

### <span data-ttu-id="7a9cd-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7a9cd-132">-InformationVariable</span></span>
<span data-ttu-id="7a9cd-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7a9cd-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="7a9cd-134">-Pre</span></span>
<span data-ttu-id="7a9cd-135">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7a9cd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a9cd-136">-ResourceGroupName</span></span>
<span data-ttu-id="7a9cd-137">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-137">The resource group name.</span></span>

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

### <span data-ttu-id="7a9cd-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a9cd-138">-SubscriptionId</span></span>
<span data-ttu-id="7a9cd-139">A használandó előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a9cd-139">The subscription to use.</span></span>

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

### <span data-ttu-id="7a9cd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9cd-140">CommonParameters</span></span>
<span data-ttu-id="7a9cd-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a9cd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9cd-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a9cd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9cd-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a9cd-143">INPUTS</span></span>

## <span data-ttu-id="7a9cd-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a9cd-144">OUTPUTS</span></span>

## <span data-ttu-id="7a9cd-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a9cd-145">NOTES</span></span>

## <span data-ttu-id="7a9cd-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a9cd-146">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 1ac0ab153177caaf080e5aa9144020ea253b8438
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301118"
---
# <span data-ttu-id="bca14-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bca14-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="bca14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bca14-102">SYNOPSIS</span></span>
<span data-ttu-id="bca14-103">Az erőforráscsoport-telepítő művelet beolvasása</span><span class="sxs-lookup"><span data-stu-id="bca14-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="bca14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bca14-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bca14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bca14-105">DESCRIPTION</span></span>
<span data-ttu-id="bca14-106">A **Get-AzResourceGroupDeploymentOperation** parancsmag a központi üzembe állítás részét képező összes műveletet felsorolja, így könnyebben megtalálhatja és megadhatja az adott üzembe állítással kapcsolatos pontos műveleteket.</span><span class="sxs-lookup"><span data-stu-id="bca14-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="bca14-107">A válasz és a kérés tartalma is megjeleníthető az egyes üzembe állítási műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="bca14-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="bca14-108">Ez a cikk a portálon található központi verzió központi telepítéséhez szükséges információkat ismerteti.</span><span class="sxs-lookup"><span data-stu-id="bca14-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="bca14-109">A kérelem és a válasz tartalmának beszerzéséhez engedélyezze a beállítást, ha a bevezetést az **új AzResourceGroupDeployment-** on keresztül küldi el.</span><span class="sxs-lookup"><span data-stu-id="bca14-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="bca14-110">Előfordulhat, hogy az erőforrás-tulajdonságokban vagy a **listKeys** -műveletekben használt jelszavakat, például a központi telepítési műveletek lekérése után visszaadott jelszavakat is naplózhatja és megjelenítheti.</span><span class="sxs-lookup"><span data-stu-id="bca14-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="bca14-111">A beállításról és annak engedélyezéséről további információt a ARM-sablonok bevezetésének New-AzResourceGroupDeployment és hibakeresése című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bca14-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="bca14-112">Példák</span><span class="sxs-lookup"><span data-stu-id="bca14-112">EXAMPLES</span></span>

### <span data-ttu-id="bca14-113">1. példa: Get1</span><span class="sxs-lookup"><span data-stu-id="bca14-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="bca14-114">A "teszt" nevű erőforráscsoport "teszt" nevű "teszt" nevű központi üzembe állítási művelete</span><span class="sxs-lookup"><span data-stu-id="bca14-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="bca14-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bca14-115">PARAMETERS</span></span>

### <span data-ttu-id="bca14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca14-116">-DefaultProfile</span></span>
<span data-ttu-id="bca14-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bca14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bca14-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="bca14-118">-DeploymentName</span></span>
<span data-ttu-id="bca14-119">A központi telepítő neve.</span><span class="sxs-lookup"><span data-stu-id="bca14-119">The deployment name.</span></span>

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

### <span data-ttu-id="bca14-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="bca14-120">-Pre</span></span>
<span data-ttu-id="bca14-121">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="bca14-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bca14-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca14-122">-ResourceGroupName</span></span>
<span data-ttu-id="bca14-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="bca14-123">The resource group name.</span></span>

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

### <span data-ttu-id="bca14-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bca14-124">-SubscriptionId</span></span>
<span data-ttu-id="bca14-125">A használandó előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bca14-125">The subscription to use.</span></span>

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

### <span data-ttu-id="bca14-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca14-126">CommonParameters</span></span>
<span data-ttu-id="bca14-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bca14-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca14-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bca14-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca14-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bca14-129">INPUTS</span></span>

### <span data-ttu-id="bca14-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bca14-130">System.String</span></span>

### <span data-ttu-id="bca14-131">System. null ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bca14-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bca14-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bca14-132">OUTPUTS</span></span>

### <span data-ttu-id="bca14-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bca14-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="bca14-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bca14-134">NOTES</span></span>

## <span data-ttu-id="bca14-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bca14-135">RELATED LINKS</span></span>

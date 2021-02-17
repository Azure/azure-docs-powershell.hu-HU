---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 1ac0ab153177caaf080e5aa9144020ea253b8438
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206015"
---
# <span data-ttu-id="c2119-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c2119-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="c2119-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2119-102">SYNOPSIS</span></span>
<span data-ttu-id="c2119-103">Az erőforráscsoport üzembe helyezésének művelete</span><span class="sxs-lookup"><span data-stu-id="c2119-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="c2119-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2119-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2119-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2119-105">DESCRIPTION</span></span>
<span data-ttu-id="c2119-106">A **Get-AzResourceGroupDeploymentOperation parancsmag** felsorolja azokat a műveleteket, amelyek egy központi telepítés részét képezték, hogy ön azonosítsa és további információt nyújtson az adott telepítés sikertelen műveleteiről.</span><span class="sxs-lookup"><span data-stu-id="c2119-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="c2119-107">Emellett az egyes telepítési műveletek válaszát és kérési tartalmát is meg tudja mutatni.</span><span class="sxs-lookup"><span data-stu-id="c2119-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="c2119-108">Ugyanezek az információk biztosítanak a portálon a központi telepítés részletei között.</span><span class="sxs-lookup"><span data-stu-id="c2119-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="c2119-109">A kérés és a választartalom lekéréséhez engedélyezze a beállítást, amikor a **New-AzResourceGroupDeployment** szolgáltatáson keresztül küld el egy központi telepítést.</span><span class="sxs-lookup"><span data-stu-id="c2119-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="c2119-110">Naplózhat és felfedhet olyan titkosságokat, például az erőforrástulajdonságban vagy a **listKeys** műveletben használt jelszavakat, amelyek az üzembe helyezési műveletek lekérésekor ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c2119-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="c2119-111">A beállításról és annak engedélyezéséről további információt a New-AzResourceGroupDeployment és ARM sablontelepítések</span><span class="sxs-lookup"><span data-stu-id="c2119-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="c2119-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2119-112">EXAMPLES</span></span>

### <span data-ttu-id="c2119-113">1. példa: Get1</span><span class="sxs-lookup"><span data-stu-id="c2119-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="c2119-114">Telepítési művelet "teszt" névvel az erőforráscsoport "teszt" csoportjában</span><span class="sxs-lookup"><span data-stu-id="c2119-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="c2119-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2119-115">PARAMETERS</span></span>

### <span data-ttu-id="c2119-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2119-116">-DefaultProfile</span></span>
<span data-ttu-id="c2119-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2119-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2119-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c2119-118">-DeploymentName</span></span>
<span data-ttu-id="c2119-119">A telepítés neve.</span><span class="sxs-lookup"><span data-stu-id="c2119-119">The deployment name.</span></span>

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

### <span data-ttu-id="c2119-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="c2119-120">-Pre</span></span>
<span data-ttu-id="c2119-121">Ha be van állítva, az azt jelenti, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="c2119-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c2119-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2119-122">-ResourceGroupName</span></span>
<span data-ttu-id="c2119-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c2119-123">The resource group name.</span></span>

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

### <span data-ttu-id="c2119-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2119-124">-SubscriptionId</span></span>
<span data-ttu-id="c2119-125">A használni használt előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2119-125">The subscription to use.</span></span>

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

### <span data-ttu-id="c2119-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2119-126">CommonParameters</span></span>
<span data-ttu-id="c2119-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2119-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2119-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2119-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2119-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2119-129">INPUTS</span></span>

### <span data-ttu-id="c2119-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c2119-130">System.String</span></span>

### <span data-ttu-id="c2119-131">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c2119-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c2119-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2119-132">OUTPUTS</span></span>

### <span data-ttu-id="c2119-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c2119-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="c2119-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2119-134">NOTES</span></span>

## <span data-ttu-id="c2119-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2119-135">RELATED LINKS</span></span>

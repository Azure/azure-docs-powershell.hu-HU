---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 761969eea685c21bc513efdfde9ea79a9e1e4a70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180984"
---
# <span data-ttu-id="f9796-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f9796-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="f9796-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9796-102">SYNOPSIS</span></span>
<span data-ttu-id="f9796-103">Beolvashatja vagy listázhatja a központi telepítő parancsfájlokat.</span><span class="sxs-lookup"><span data-stu-id="f9796-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="f9796-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9796-104">SYNTAX</span></span>

### <span data-ttu-id="f9796-105">ListDeploymentScript (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9796-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9796-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="f9796-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9796-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9796-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9796-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9796-108">DESCRIPTION</span></span>
<span data-ttu-id="f9796-109">A **Get-AzDeploymentScript** parancsmag egyetlen telepítő parancsfájlt vagy telepítő parancsfájlok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="f9796-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="f9796-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f9796-110">EXAMPLES</span></span>

### <span data-ttu-id="f9796-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f9796-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="f9796-112">Az előfizetésben lévő központi telepítő parancsfájlok listája az aktuális felhasználó környezetében.</span><span class="sxs-lookup"><span data-stu-id="f9796-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="f9796-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f9796-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="f9796-114">Az erőforráscsoport-telepítő parancsfájlok listája az erőforráscsoport DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="f9796-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="f9796-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="f9796-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="f9796-116">Beolvassa a MyDeploymentScript nevű telepítő parancsfájlt az erőforráscsoport DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="f9796-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="f9796-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="f9796-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="f9796-118">A megadott erőforrás-azonosítóval rendelkező központi telepítő parancsfájlt kap.</span><span class="sxs-lookup"><span data-stu-id="f9796-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="f9796-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9796-119">PARAMETERS</span></span>

### <span data-ttu-id="f9796-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9796-120">-DefaultProfile</span></span>
<span data-ttu-id="f9796-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9796-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9796-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="f9796-122">-Id</span></span>
<span data-ttu-id="f9796-123">A telepítő parancsfájl teljes mértékben minősített erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f9796-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="f9796-124">Példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="f9796-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9796-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9796-125">-Name</span></span>
<span data-ttu-id="f9796-126">A telepítő parancsfájl neve</span><span class="sxs-lookup"><span data-stu-id="f9796-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9796-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9796-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9796-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9796-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9796-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9796-129">CommonParameters</span></span>
<span data-ttu-id="f9796-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9796-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f9796-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9796-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9796-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9796-132">INPUTS</span></span>

### <span data-ttu-id="f9796-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f9796-133">System.String</span></span>

## <span data-ttu-id="f9796-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9796-134">OUTPUTS</span></span>

### <span data-ttu-id="f9796-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f9796-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="f9796-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9796-136">NOTES</span></span>

## <span data-ttu-id="f9796-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9796-137">RELATED LINKS</span></span>

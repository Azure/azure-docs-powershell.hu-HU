---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 761969eea685c21bc513efdfde9ea79a9e1e4a70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012324"
---
# <span data-ttu-id="77edc-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="77edc-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="77edc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77edc-102">SYNOPSIS</span></span>
<span data-ttu-id="77edc-103">Beolvashatja vagy listázhatja a központi telepítő parancsfájlokat.</span><span class="sxs-lookup"><span data-stu-id="77edc-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="77edc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77edc-104">SYNTAX</span></span>

### <span data-ttu-id="77edc-105">ListDeploymentScript (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77edc-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77edc-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="77edc-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77edc-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="77edc-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77edc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="77edc-108">DESCRIPTION</span></span>
<span data-ttu-id="77edc-109">A **Get-AzDeploymentScript** parancsmag egyetlen telepítő parancsfájlt vagy telepítő parancsfájlok listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="77edc-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="77edc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="77edc-110">EXAMPLES</span></span>

### <span data-ttu-id="77edc-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="77edc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="77edc-112">Az előfizetésben lévő központi telepítő parancsfájlok listája az aktuális felhasználó környezetében.</span><span class="sxs-lookup"><span data-stu-id="77edc-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="77edc-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="77edc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="77edc-114">Az erőforráscsoport-telepítő parancsfájlok listája az erőforráscsoport DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="77edc-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="77edc-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="77edc-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="77edc-116">Beolvassa a MyDeploymentScript nevű telepítő parancsfájlt az erőforráscsoport DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="77edc-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="77edc-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="77edc-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="77edc-118">A megadott erőforrás-azonosítóval rendelkező központi telepítő parancsfájlt kap.</span><span class="sxs-lookup"><span data-stu-id="77edc-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="77edc-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77edc-119">PARAMETERS</span></span>

### <span data-ttu-id="77edc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77edc-120">-DefaultProfile</span></span>
<span data-ttu-id="77edc-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77edc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77edc-122">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="77edc-122">-Id</span></span>
<span data-ttu-id="77edc-123">A telepítő parancsfájl teljes mértékben minősített erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="77edc-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="77edc-124">Példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="77edc-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="77edc-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77edc-125">-Name</span></span>
<span data-ttu-id="77edc-126">A telepítő parancsfájl neve</span><span class="sxs-lookup"><span data-stu-id="77edc-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="77edc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77edc-127">-ResourceGroupName</span></span>
<span data-ttu-id="77edc-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="77edc-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="77edc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77edc-129">CommonParameters</span></span>
<span data-ttu-id="77edc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77edc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="77edc-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77edc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77edc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77edc-132">INPUTS</span></span>

### <span data-ttu-id="77edc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="77edc-133">System.String</span></span>

## <span data-ttu-id="77edc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77edc-134">OUTPUTS</span></span>

### <span data-ttu-id="77edc-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="77edc-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="77edc-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77edc-136">NOTES</span></span>

## <span data-ttu-id="77edc-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77edc-137">RELATED LINKS</span></span>

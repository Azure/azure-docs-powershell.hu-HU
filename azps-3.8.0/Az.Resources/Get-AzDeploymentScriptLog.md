---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014319"
---
# <span data-ttu-id="bf269-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="bf269-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="bf269-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf269-102">SYNOPSIS</span></span>
<span data-ttu-id="bf269-103">Beolvassa a központi telepítő parancsfájl-végrehajtás naplózását.</span><span class="sxs-lookup"><span data-stu-id="bf269-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="bf269-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf269-104">SYNTAX</span></span>

### <span data-ttu-id="bf269-105">GetDeploymentScriptLogByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf269-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf269-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf269-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf269-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf269-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf269-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf269-108">DESCRIPTION</span></span>
<span data-ttu-id="bf269-109">A **Get-AzDeploymentScriptLog** parancsmag a telepítő parancsfájl-végrehajtás naplózását kapja.</span><span class="sxs-lookup"><span data-stu-id="bf269-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="bf269-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bf269-110">EXAMPLES</span></span>

### <span data-ttu-id="bf269-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf269-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="bf269-112">Beolvassa a MyDeploymentScript nevű központi telepítő parancsfájlt az erőforráscsoport DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="bf269-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="bf269-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bf269-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="bf269-114">Az első parancs beolvassa a MyDeploymentScript nevű központi telepítő parancsfájlt az erőforráscsoport DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="bf269-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="bf269-115">A második parancs a központi telepítő parancsfájl naplójába kerül.</span><span class="sxs-lookup"><span data-stu-id="bf269-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="bf269-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf269-116">PARAMETERS</span></span>

### <span data-ttu-id="bf269-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf269-117">-DefaultProfile</span></span>
<span data-ttu-id="bf269-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf269-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf269-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="bf269-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="bf269-120">A telepítő parancsfájl PowerShell-objektuma.</span><span class="sxs-lookup"><span data-stu-id="bf269-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf269-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="bf269-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="bf269-122">A telepítő parancsfájl teljes mértékben minősített erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bf269-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="bf269-123">Példa:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="bf269-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf269-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf269-124">-Name</span></span>
<span data-ttu-id="bf269-125">A telepítő parancsfájl neve.</span><span class="sxs-lookup"><span data-stu-id="bf269-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf269-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf269-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf269-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bf269-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf269-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf269-128">CommonParameters</span></span>
<span data-ttu-id="bf269-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf269-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bf269-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf269-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf269-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf269-131">INPUTS</span></span>

### <span data-ttu-id="bf269-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bf269-132">System.String</span></span>

### <span data-ttu-id="bf269-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="bf269-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="bf269-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf269-134">OUTPUTS</span></span>

### <span data-ttu-id="bf269-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="bf269-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="bf269-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf269-136">NOTES</span></span>

## <span data-ttu-id="bf269-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf269-137">RELATED LINKS</span></span>

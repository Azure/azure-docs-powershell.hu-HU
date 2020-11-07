---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 97fbda90b27cbfabca8cbfd21c5bf375b86f7adb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849453"
---
# <span data-ttu-id="84aa0-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84aa0-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="84aa0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="84aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="84aa0-103">Egy erőforráscsoport-telepítő érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="84aa0-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84aa0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="84aa0-104">SYNTAX</span></span>

### <span data-ttu-id="84aa0-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84aa0-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84aa0-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="84aa0-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84aa0-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="84aa0-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84aa0-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="84aa0-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84aa0-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="84aa0-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84aa0-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="84aa0-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84aa0-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="84aa0-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84aa0-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="84aa0-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84aa0-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="84aa0-113">DESCRIPTION</span></span>
<span data-ttu-id="84aa0-114">A **AzureRmResourceGroupDeployment** parancsmag azt határozza meg, hogy egy Azure erőforráscsoport-telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="84aa0-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="84aa0-115">Példák</span><span class="sxs-lookup"><span data-stu-id="84aa0-115">EXAMPLES</span></span>

## <span data-ttu-id="84aa0-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="84aa0-116">PARAMETERS</span></span>

### <span data-ttu-id="84aa0-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="84aa0-117">-ApiVersion</span></span>
<span data-ttu-id="84aa0-118">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="84aa0-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="84aa0-119">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="84aa0-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="84aa0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84aa0-120">-DefaultProfile</span></span>
<span data-ttu-id="84aa0-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="84aa0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84aa0-122">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="84aa0-122">-Mode</span></span>
<span data-ttu-id="84aa0-123">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="84aa0-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="84aa0-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="84aa0-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="84aa0-125">Növekményes</span><span class="sxs-lookup"><span data-stu-id="84aa0-125">Incremental</span></span>
- <span data-ttu-id="84aa0-126">Teljes</span><span class="sxs-lookup"><span data-stu-id="84aa0-126">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="84aa0-127">-Pre</span></span>
<span data-ttu-id="84aa0-128">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="84aa0-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="84aa0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84aa0-129">-ResourceGroupName</span></span>
<span data-ttu-id="84aa0-130">A tesztelni kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84aa0-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="84aa0-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="84aa0-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="84aa0-132">Ha az erőforrás csoportban az adott nevű névvel a sikeres telepítésre szeretne visszagörgetni, akkor ne használja a ha-RollbackToLastDeployment használatát.</span><span class="sxs-lookup"><span data-stu-id="84aa0-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="84aa0-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="84aa0-134">Az erőforrás csoport utolsó sikeres telepítésére való visszagörgetéskor ne legyen megjelenni, ha-RollBackDeploymentName használja.</span><span class="sxs-lookup"><span data-stu-id="84aa0-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="84aa0-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="84aa0-135">-TemplateFile</span></span>
<span data-ttu-id="84aa0-136">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84aa0-136">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="84aa0-137">-TemplateParameterFile</span></span>
<span data-ttu-id="84aa0-138">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84aa0-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="84aa0-139">-TemplateParameterObject</span></span>
<span data-ttu-id="84aa0-140">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="84aa0-140">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="84aa0-141">-TemplateParameterUri</span></span>
<span data-ttu-id="84aa0-142">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="84aa0-142">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="84aa0-143">-TemplateUri</span></span>
<span data-ttu-id="84aa0-144">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="84aa0-144">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84aa0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84aa0-145">CommonParameters</span></span>
<span data-ttu-id="84aa0-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="84aa0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84aa0-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84aa0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84aa0-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="84aa0-148">INPUTS</span></span>

### <span data-ttu-id="84aa0-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="84aa0-149">None</span></span>

## <span data-ttu-id="84aa0-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84aa0-150">OUTPUTS</span></span>

### <span data-ttu-id="84aa0-151">Microsoft. Azure. Command. ResourceManager. models. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="84aa0-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="84aa0-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="84aa0-152">NOTES</span></span>

## <span data-ttu-id="84aa0-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84aa0-153">RELATED LINKS</span></span>

[<span data-ttu-id="84aa0-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84aa0-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="84aa0-155">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84aa0-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="84aa0-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84aa0-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="84aa0-157">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="84aa0-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)



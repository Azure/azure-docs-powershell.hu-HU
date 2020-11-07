---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 59bbe7c5309764c41f22aaa99dbb4d47a23f1ba8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843169"
---
# <span data-ttu-id="f751e-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f751e-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="f751e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f751e-102">SYNOPSIS</span></span>
<span data-ttu-id="f751e-103">Egy erőforráscsoport-telepítő érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="f751e-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="f751e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f751e-104">SYNTAX</span></span>

### <span data-ttu-id="f751e-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f751e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f751e-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f751e-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f751e-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f751e-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f751e-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f751e-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f751e-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f751e-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f751e-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f751e-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f751e-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f751e-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f751e-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f751e-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f751e-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="f751e-113">DESCRIPTION</span></span>
<span data-ttu-id="f751e-114">A **AzResourceGroupDeployment** parancsmag azt határozza meg, hogy egy Azure erőforráscsoport-telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="f751e-114">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f751e-115">Példák</span><span class="sxs-lookup"><span data-stu-id="f751e-115">EXAMPLES</span></span>

## <span data-ttu-id="f751e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f751e-116">PARAMETERS</span></span>

### <span data-ttu-id="f751e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f751e-117">-ApiVersion</span></span>
<span data-ttu-id="f751e-118">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f751e-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f751e-119">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="f751e-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f751e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f751e-120">-DefaultProfile</span></span>
<span data-ttu-id="f751e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f751e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f751e-122">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="f751e-122">-Mode</span></span>
<span data-ttu-id="f751e-123">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f751e-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="f751e-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f751e-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f751e-125">Növekményes</span><span class="sxs-lookup"><span data-stu-id="f751e-125">Incremental</span></span>
- <span data-ttu-id="f751e-126">Teljes</span><span class="sxs-lookup"><span data-stu-id="f751e-126">Complete</span></span>

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

### <span data-ttu-id="f751e-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="f751e-127">-Pre</span></span>
<span data-ttu-id="f751e-128">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f751e-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f751e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f751e-129">-ResourceGroupName</span></span>
<span data-ttu-id="f751e-130">A tesztelni kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f751e-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="f751e-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="f751e-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="f751e-132">Ha az erőforrás csoportban az adott nevű névvel a sikeres telepítésre szeretne visszagörgetni, akkor ne használja a ha-RollbackToLastDeployment használatát.</span><span class="sxs-lookup"><span data-stu-id="f751e-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="f751e-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="f751e-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="f751e-134">Az erőforrás csoport utolsó sikeres telepítésére való visszagörgetéskor ne legyen megjelenni, ha-RollBackDeploymentName használja.</span><span class="sxs-lookup"><span data-stu-id="f751e-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="f751e-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f751e-135">-TemplateFile</span></span>
<span data-ttu-id="f751e-136">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f751e-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="f751e-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f751e-137">-TemplateParameterFile</span></span>
<span data-ttu-id="f751e-138">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f751e-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="f751e-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f751e-139">-TemplateParameterObject</span></span>
<span data-ttu-id="f751e-140">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f751e-140">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="f751e-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f751e-141">-TemplateParameterUri</span></span>
<span data-ttu-id="f751e-142">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f751e-142">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="f751e-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f751e-143">-TemplateUri</span></span>
<span data-ttu-id="f751e-144">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f751e-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="f751e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f751e-145">CommonParameters</span></span>
<span data-ttu-id="f751e-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f751e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f751e-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f751e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f751e-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f751e-148">INPUTS</span></span>

### <span data-ttu-id="f751e-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="f751e-149">None</span></span>

## <span data-ttu-id="f751e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f751e-150">OUTPUTS</span></span>

### <span data-ttu-id="f751e-151">Microsoft. Azure. Command. ResourceManager. models. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f751e-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="f751e-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f751e-152">NOTES</span></span>

## <span data-ttu-id="f751e-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f751e-153">RELATED LINKS</span></span>

[<span data-ttu-id="f751e-154">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f751e-154">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="f751e-155">Új – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f751e-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="f751e-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f751e-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="f751e-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f751e-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)



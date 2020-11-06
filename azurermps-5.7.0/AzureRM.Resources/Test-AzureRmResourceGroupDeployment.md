---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502451"
---
# <span data-ttu-id="b5495-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b5495-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b5495-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5495-102">SYNOPSIS</span></span>
<span data-ttu-id="b5495-103">Egy erőforráscsoport-telepítő érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="b5495-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5495-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5495-104">SYNTAX</span></span>

### <span data-ttu-id="b5495-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5495-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5495-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b5495-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5495-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b5495-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5495-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b5495-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5495-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b5495-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5495-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b5495-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5495-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b5495-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5495-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b5495-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5495-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5495-113">DESCRIPTION</span></span>
<span data-ttu-id="b5495-114">A **AzureRmResourceGroupDeployment** parancsmag azt határozza meg, hogy egy Azure erőforráscsoport-telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="b5495-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="b5495-115">Példák</span><span class="sxs-lookup"><span data-stu-id="b5495-115">EXAMPLES</span></span>

## <span data-ttu-id="b5495-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5495-116">PARAMETERS</span></span>

### <span data-ttu-id="b5495-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b5495-117">-ApiVersion</span></span>
<span data-ttu-id="b5495-118">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5495-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b5495-119">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="b5495-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b5495-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5495-120">-DefaultProfile</span></span>
<span data-ttu-id="b5495-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b5495-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5495-122">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="b5495-122">-Mode</span></span>
<span data-ttu-id="b5495-123">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5495-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="b5495-124">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="b5495-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5495-125">Növekményes</span><span class="sxs-lookup"><span data-stu-id="b5495-125">Incremental</span></span>
- <span data-ttu-id="b5495-126">Teljes</span><span class="sxs-lookup"><span data-stu-id="b5495-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="b5495-127">-Pre</span></span>
<span data-ttu-id="b5495-128">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="b5495-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b5495-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5495-129">-ResourceGroupName</span></span>
<span data-ttu-id="b5495-130">A tesztelni kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5495-130">Specifies the name of the resource group to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-131">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b5495-131">-TemplateFile</span></span>
<span data-ttu-id="b5495-132">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5495-132">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b5495-133">-TemplateParameterFile</span></span>
<span data-ttu-id="b5495-134">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5495-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b5495-135">-TemplateParameterObject</span></span>
<span data-ttu-id="b5495-136">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5495-136">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b5495-137">-TemplateParameterUri</span></span>
<span data-ttu-id="b5495-138">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5495-138">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b5495-139">-TemplateUri</span></span>
<span data-ttu-id="b5495-140">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5495-140">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5495-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5495-141">CommonParameters</span></span>
<span data-ttu-id="b5495-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5495-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5495-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5495-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5495-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5495-144">INPUTS</span></span>

### <span data-ttu-id="b5495-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5495-145">None</span></span>
<span data-ttu-id="b5495-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="b5495-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5495-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5495-147">OUTPUTS</span></span>

### <span data-ttu-id="b5495-148">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="b5495-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="b5495-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5495-149">NOTES</span></span>

## <span data-ttu-id="b5495-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5495-150">RELATED LINKS</span></span>

[<span data-ttu-id="b5495-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b5495-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b5495-152">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b5495-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b5495-153">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b5495-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b5495-154">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b5495-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)



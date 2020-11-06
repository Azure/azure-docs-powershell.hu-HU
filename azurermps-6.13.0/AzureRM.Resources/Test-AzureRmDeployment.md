---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmDeployment.md
ms.openlocfilehash: fdfef01f9ba8013b25db227c0833a7add408c490
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494938"
---
# <span data-ttu-id="f743c-101">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="f743c-101">Test-AzureRmDeployment</span></span>

## <span data-ttu-id="f743c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f743c-102">SYNOPSIS</span></span>
<span data-ttu-id="f743c-103">Ellenőrzi a központi telepítőt.</span><span class="sxs-lookup"><span data-stu-id="f743c-103">Validates a deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f743c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f743c-104">SYNTAX</span></span>

### <span data-ttu-id="f743c-105">ByTemplateFileWithNoParameters (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f743c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f743c-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f743c-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f743c-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f743c-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f743c-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f743c-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f743c-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f743c-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f743c-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f743c-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f743c-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f743c-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f743c-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f743c-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f743c-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="f743c-113">DESCRIPTION</span></span>
<span data-ttu-id="f743c-114">A **AzureRmDeployment** parancsmag azt határozza meg, hogy a központi telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="f743c-114">The **Test-AzureRmDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f743c-115">Példák</span><span class="sxs-lookup"><span data-stu-id="f743c-115">EXAMPLES</span></span>

### <span data-ttu-id="f743c-116">1. példa: a bevezetést tesztelheti egyéni sablonnal és paraméteres fájllal</span><span class="sxs-lookup"><span data-stu-id="f743c-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="f743c-117">Ez a parancs az aktuális előfizetési tartományon alapuló központi telepítés tesztelésére szolgál a megadott sablonfájl és a parameters (sablonfájl) fájllal.</span><span class="sxs-lookup"><span data-stu-id="f743c-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="f743c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f743c-118">PARAMETERS</span></span>

### <span data-ttu-id="f743c-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f743c-119">-ApiVersion</span></span>
<span data-ttu-id="f743c-120">Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f743c-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f743c-121">Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f743c-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f743c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f743c-122">-DefaultProfile</span></span>
<span data-ttu-id="f743c-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f743c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f743c-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="f743c-124">-Location</span></span>
<span data-ttu-id="f743c-125">A központi telepítő adatainak tárolására szolgáló hely.</span><span class="sxs-lookup"><span data-stu-id="f743c-125">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f743c-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="f743c-126">-Pre</span></span>
<span data-ttu-id="f743c-127">Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f743c-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f743c-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f743c-128">-TemplateFile</span></span>
<span data-ttu-id="f743c-129">A sablonfájl helyi elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f743c-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="f743c-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f743c-130">-TemplateParameterFile</span></span>
<span data-ttu-id="f743c-131">A sablon paramétereit tartalmazó fájl</span><span class="sxs-lookup"><span data-stu-id="f743c-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="f743c-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f743c-132">-TemplateParameterObject</span></span>
<span data-ttu-id="f743c-133">A paramétereket jelképező kivonatoló táblázat.</span><span class="sxs-lookup"><span data-stu-id="f743c-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="f743c-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f743c-134">-TemplateParameterUri</span></span>
<span data-ttu-id="f743c-135">URI a sablon paraméter-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="f743c-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="f743c-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f743c-136">-TemplateUri</span></span>
<span data-ttu-id="f743c-137">A sablonfájl URI-ja.</span><span class="sxs-lookup"><span data-stu-id="f743c-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="f743c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f743c-138">CommonParameters</span></span>
<span data-ttu-id="f743c-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f743c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f743c-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f743c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f743c-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f743c-141">INPUTS</span></span>

### <span data-ttu-id="f743c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f743c-142">System.String</span></span>
<span data-ttu-id="f743c-143">Microsoft. Azure. Management. ResourceManager. models. DeploymentMode. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f743c-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="f743c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f743c-144">OUTPUTS</span></span>

### <span data-ttu-id="f743c-145">Microsoft. Azure. Command. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f743c-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="f743c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f743c-146">NOTES</span></span>

## <span data-ttu-id="f743c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f743c-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496924"
---
# <span data-ttu-id="f8cfc-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8cfc-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f8cfc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="f8cfc-103">Egy erőforráscsoport-telepítő érvényesítése.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8cfc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8cfc-104">SYNTAX</span></span>

### <span data-ttu-id="f8cfc-105">Telepítés sablonon keresztül paraméterek nélkül (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8cfc-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8cfc-106">Telepítés sablonfájl és sablon paraméterei objektum segítségével</span><span class="sxs-lookup"><span data-stu-id="f8cfc-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8cfc-107">Telepítés sablon URI és sablon paraméterei objektum segítségével</span><span class="sxs-lookup"><span data-stu-id="f8cfc-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8cfc-108">Telepítés sablonfájl és sablon paraméterei fájl segítségével</span><span class="sxs-lookup"><span data-stu-id="f8cfc-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8cfc-109">A telepítés sablon URI és sablon paraméterei fájl segítségével</span><span class="sxs-lookup"><span data-stu-id="f8cfc-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8cfc-110">Telepítés sablonon keresztüli sablon paramétereit tartalmazó URI-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="f8cfc-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8cfc-111">Telepítés sablon URI-és sablon-paraméterek URI-kapcsolaton keresztül</span><span class="sxs-lookup"><span data-stu-id="f8cfc-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8cfc-112">Bevezetés a Template URI-ba paraméterek nélkül</span><span class="sxs-lookup"><span data-stu-id="f8cfc-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8cfc-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8cfc-113">DESCRIPTION</span></span>
<span data-ttu-id="f8cfc-114">A **AzureRmResourceGroupDeployment** parancsmag azt határozza meg, hogy egy Azure erőforráscsoport-telepítő sablon és a paraméter értéke érvényes-e.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f8cfc-115">Példák</span><span class="sxs-lookup"><span data-stu-id="f8cfc-115">EXAMPLES</span></span>

## <span data-ttu-id="f8cfc-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8cfc-116">PARAMETERS</span></span>

### <span data-ttu-id="f8cfc-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f8cfc-117">-ApiVersion</span></span>
<span data-ttu-id="f8cfc-118">Az erőforrás-szolgáltató által támogatott API-verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f8cfc-119">Az alapértelmezett verziótól eltérő verziót is megadhat.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f8cfc-120">Üzemmód</span><span class="sxs-lookup"><span data-stu-id="f8cfc-120">-Mode</span></span>
<span data-ttu-id="f8cfc-121">A telepítő üzemmódot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="f8cfc-122">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f8cfc-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f8cfc-123">Növekményes</span><span class="sxs-lookup"><span data-stu-id="f8cfc-123">Incremental</span></span>
- <span data-ttu-id="f8cfc-124">Teljes</span><span class="sxs-lookup"><span data-stu-id="f8cfc-124">Complete</span></span>

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

### <span data-ttu-id="f8cfc-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="f8cfc-125">-Pre</span></span>
<span data-ttu-id="f8cfc-126">Jelzi, hogy ez a parancsmag az előzetes verziójú API-verziókat veszi figyelembe, amikor az automatikusan meghatározza, hogy melyik verziót használja.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f8cfc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8cfc-127">-ResourceGroupName</span></span>
<span data-ttu-id="f8cfc-128">A tesztelni kívánt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-128">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="f8cfc-129">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f8cfc-129">-TemplateFile</span></span>
<span data-ttu-id="f8cfc-130">A JSON-sablonfájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cfc-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f8cfc-131">-TemplateParameterFile</span></span>
<span data-ttu-id="f8cfc-132">A sablon paramétereinek nevét és értékét tartalmazó JSON-fájl teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cfc-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f8cfc-133">-TemplateParameterObject</span></span>
<span data-ttu-id="f8cfc-134">A Template paraméterek neveinek és értékeinek hash-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cfc-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f8cfc-135">-TemplateParameterUri</span></span>
<span data-ttu-id="f8cfc-136">A sablon paramétereinek fájljának URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cfc-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f8cfc-137">-TemplateUri</span></span>
<span data-ttu-id="f8cfc-138">A JSON sablonfájl URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cfc-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8cfc-139">-DefaultProfile</span></span>
<span data-ttu-id="f8cfc-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8cfc-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8cfc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8cfc-141">CommonParameters</span></span>
<span data-ttu-id="f8cfc-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8cfc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8cfc-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8cfc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8cfc-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8cfc-144">INPUTS</span></span>

## <span data-ttu-id="f8cfc-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8cfc-145">OUTPUTS</span></span>

### <span data-ttu-id="f8cfc-146">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. ResourceManager. Parancsmags. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="f8cfc-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="f8cfc-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8cfc-147">NOTES</span></span>

## <span data-ttu-id="f8cfc-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8cfc-148">RELATED LINKS</span></span>

[<span data-ttu-id="f8cfc-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8cfc-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f8cfc-150">Új – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8cfc-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f8cfc-151">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8cfc-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f8cfc-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f8cfc-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)



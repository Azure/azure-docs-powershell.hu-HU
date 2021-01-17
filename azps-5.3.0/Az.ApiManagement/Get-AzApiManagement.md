---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479029"
---
# <span data-ttu-id="370c1-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="370c1-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="370c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="370c1-102">SYNOPSIS</span></span>
<span data-ttu-id="370c1-103">Listát vagy adott API Management Service-leírást kap.</span><span class="sxs-lookup"><span data-stu-id="370c1-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="370c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="370c1-104">SYNTAX</span></span>

### <span data-ttu-id="370c1-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="370c1-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="370c1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="370c1-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="370c1-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="370c1-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="370c1-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="370c1-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="370c1-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="370c1-109">DESCRIPTION</span></span>
<span data-ttu-id="370c1-110">A **Get-AzApiManagement** parancsmag lekérte az előfizetés vagy adott erőforráscsoport vagy adott API-kezelés alatt található ÖSSZES API-kezelési szolgáltatás listáját.</span><span class="sxs-lookup"><span data-stu-id="370c1-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="370c1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="370c1-111">EXAMPLES</span></span>

### <span data-ttu-id="370c1-112">1. példa: Az összes API-kezelési szolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="370c1-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="370c1-113">Ez a parancs egy előfizetésen belül az összes API-kezelési szolgáltatást lekérte.</span><span class="sxs-lookup"><span data-stu-id="370c1-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="370c1-114">2. példa: Az összes API-kezelési szolgáltatás lekérte egy adott névvel</span><span class="sxs-lookup"><span data-stu-id="370c1-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="370c1-115">Ez a parancs név szerint kapja meg az összes API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="370c1-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="370c1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="370c1-116">PARAMETERS</span></span>

### <span data-ttu-id="370c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370c1-117">-DefaultProfile</span></span>
<span data-ttu-id="370c1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="370c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="370c1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="370c1-119">-Name</span></span>
<span data-ttu-id="370c1-120">Az API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="370c1-120">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370c1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="370c1-121">-ResourceGroupName</span></span>
<span data-ttu-id="370c1-122">Annak az erőforráscsoportnak a nevét adja meg, amely alatt ez a parancsmag az API-kezelési szolgáltatást kapja.</span><span class="sxs-lookup"><span data-stu-id="370c1-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370c1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="370c1-123">-ResourceId</span></span>
<span data-ttu-id="370c1-124">Arm ResourceId of the API Management service.</span><span class="sxs-lookup"><span data-stu-id="370c1-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370c1-125">CommonParameters</span></span>
<span data-ttu-id="370c1-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="370c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370c1-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="370c1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370c1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="370c1-128">INPUTS</span></span>

### <span data-ttu-id="370c1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="370c1-129">System.String</span></span>

## <span data-ttu-id="370c1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="370c1-130">OUTPUTS</span></span>

### <span data-ttu-id="370c1-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="370c1-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="370c1-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="370c1-132">NOTES</span></span>

## <span data-ttu-id="370c1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="370c1-133">RELATED LINKS</span></span>

[<span data-ttu-id="370c1-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="370c1-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="370c1-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="370c1-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="370c1-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="370c1-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="370c1-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="370c1-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)



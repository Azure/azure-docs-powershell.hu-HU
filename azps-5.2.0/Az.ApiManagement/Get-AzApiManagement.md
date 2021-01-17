---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340133"
---
# <span data-ttu-id="3a805-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a805-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="3a805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a805-102">SYNOPSIS</span></span>
<span data-ttu-id="3a805-103">Listát vagy adott API Management Service-leírást kap.</span><span class="sxs-lookup"><span data-stu-id="3a805-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="3a805-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3a805-104">SYNTAX</span></span>

### <span data-ttu-id="3a805-105">GetBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a805-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a805-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a805-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a805-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="3a805-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a805-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a805-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a805-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3a805-109">DESCRIPTION</span></span>
<span data-ttu-id="3a805-110">A **Get-AzApiManagement** parancsmag lekérte az előfizetés vagy adott erőforráscsoport vagy adott API-kezelés alatt található ÖSSZES API-kezelési szolgáltatás listáját.</span><span class="sxs-lookup"><span data-stu-id="3a805-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="3a805-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3a805-111">EXAMPLES</span></span>

### <span data-ttu-id="3a805-112">1. példa: Az összes API-kezelési szolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="3a805-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="3a805-113">Ez a parancs egy előfizetésen belül az összes API-kezelési szolgáltatást lekérte.</span><span class="sxs-lookup"><span data-stu-id="3a805-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="3a805-114">2. példa: Az összes API-kezelési szolgáltatás lekérte egy adott névvel</span><span class="sxs-lookup"><span data-stu-id="3a805-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="3a805-115">Ez a parancs név szerint kapja meg az összes API-kezelési szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="3a805-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="3a805-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a805-116">PARAMETERS</span></span>

### <span data-ttu-id="3a805-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a805-117">-DefaultProfile</span></span>
<span data-ttu-id="3a805-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a805-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a805-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3a805-119">-Name</span></span>
<span data-ttu-id="3a805-120">Az API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a805-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="3a805-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a805-121">-ResourceGroupName</span></span>
<span data-ttu-id="3a805-122">Annak az erőforráscsoportnak a nevét adja meg, amely alatt ez a parancsmag az API-kezelési szolgáltatást kapja.</span><span class="sxs-lookup"><span data-stu-id="3a805-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="3a805-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a805-123">-ResourceId</span></span>
<span data-ttu-id="3a805-124">Arm ResourceId of the API Management service.</span><span class="sxs-lookup"><span data-stu-id="3a805-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="3a805-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a805-125">CommonParameters</span></span>
<span data-ttu-id="3a805-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a805-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a805-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a805-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a805-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a805-128">INPUTS</span></span>

### <span data-ttu-id="3a805-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3a805-129">System.String</span></span>

## <span data-ttu-id="3a805-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a805-130">OUTPUTS</span></span>

### <span data-ttu-id="3a805-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a805-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3a805-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3a805-132">NOTES</span></span>

## <span data-ttu-id="3a805-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a805-133">RELATED LINKS</span></span>

[<span data-ttu-id="3a805-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a805-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="3a805-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a805-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="3a805-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a805-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="3a805-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a805-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)



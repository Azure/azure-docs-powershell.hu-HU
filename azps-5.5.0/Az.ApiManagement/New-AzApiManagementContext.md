---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162643"
---
# <span data-ttu-id="860bf-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="860bf-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="860bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="860bf-102">SYNOPSIS</span></span>
<span data-ttu-id="860bf-103">Létrehozza a PsAzureApiManagementContext egy példányát.</span><span class="sxs-lookup"><span data-stu-id="860bf-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="860bf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="860bf-104">SYNTAX</span></span>

### <span data-ttu-id="860bf-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="860bf-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="860bf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="860bf-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="860bf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="860bf-107">DESCRIPTION</span></span>
<span data-ttu-id="860bf-108">A **New-AzApiManagementContext** parancsmag létrehozza a **PsAzureApiManagementContext egy példányát.**</span><span class="sxs-lookup"><span data-stu-id="860bf-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="860bf-109">A környezet az összes API Felügyeleti szolgáltatás parancsmaghoz használatos.</span><span class="sxs-lookup"><span data-stu-id="860bf-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="860bf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="860bf-110">EXAMPLES</span></span>

### <span data-ttu-id="860bf-111">1. példa: PsApiManagementContext példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="860bf-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="860bf-112">Ez a parancs létrehozza a **PsApiManagementContext egy példányát.**</span><span class="sxs-lookup"><span data-stu-id="860bf-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="860bf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="860bf-113">PARAMETERS</span></span>

### <span data-ttu-id="860bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860bf-114">-DefaultProfile</span></span>
<span data-ttu-id="860bf-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="860bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="860bf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860bf-116">-ResourceGroupName</span></span>
<span data-ttu-id="860bf-117">Annak az erőforráscsoportnak a nevét adja meg, amely alatt az API-kezelési szolgáltatás telepítve van.</span><span class="sxs-lookup"><span data-stu-id="860bf-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860bf-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="860bf-118">-ResourceId</span></span>
<span data-ttu-id="860bf-119">ApiManagement-szolgáltatás arm resource identifierje.</span><span class="sxs-lookup"><span data-stu-id="860bf-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="860bf-120">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="860bf-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860bf-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="860bf-121">-ServiceName</span></span>
<span data-ttu-id="860bf-122">A telepített API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="860bf-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860bf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860bf-123">CommonParameters</span></span>
<span data-ttu-id="860bf-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860bf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860bf-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="860bf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860bf-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="860bf-126">INPUTS</span></span>

### <span data-ttu-id="860bf-127">System.String</span><span class="sxs-lookup"><span data-stu-id="860bf-127">System.String</span></span>

## <span data-ttu-id="860bf-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="860bf-128">OUTPUTS</span></span>

### <span data-ttu-id="860bf-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="860bf-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="860bf-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="860bf-130">NOTES</span></span>

## <span data-ttu-id="860bf-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="860bf-131">RELATED LINKS</span></span>

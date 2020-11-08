---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012243"
---
# <span data-ttu-id="01033-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01033-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="01033-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="01033-102">SYNOPSIS</span></span>
<span data-ttu-id="01033-103">Létrehozza a PsAzureApiManagementContext példányát.</span><span class="sxs-lookup"><span data-stu-id="01033-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="01033-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="01033-104">SYNTAX</span></span>

### <span data-ttu-id="01033-105">ContextParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01033-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01033-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01033-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01033-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="01033-107">DESCRIPTION</span></span>
<span data-ttu-id="01033-108">A **New-AzApiManagementContext** parancsmag a **PsAzureApiManagementContext** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="01033-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="01033-109">A környezet az API-kezelési szolgáltatás összes parancsmagja esetén használatos.</span><span class="sxs-lookup"><span data-stu-id="01033-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="01033-110">Példák</span><span class="sxs-lookup"><span data-stu-id="01033-110">EXAMPLES</span></span>

### <span data-ttu-id="01033-111">1. példa: PsApiManagementContext-példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="01033-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="01033-112">Ez a parancs létrehoz egy **PsApiManagementContext** -példányt.</span><span class="sxs-lookup"><span data-stu-id="01033-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="01033-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="01033-113">PARAMETERS</span></span>

### <span data-ttu-id="01033-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01033-114">-DefaultProfile</span></span>
<span data-ttu-id="01033-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01033-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01033-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01033-116">-ResourceGroupName</span></span>
<span data-ttu-id="01033-117">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt egy API-kezelési szolgáltatás van telepítve.</span><span class="sxs-lookup"><span data-stu-id="01033-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="01033-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01033-118">-ResourceId</span></span>
<span data-ttu-id="01033-119">A ApiManagement szolgáltatás ARM erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="01033-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="01033-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="01033-120">This parameter is required.</span></span>

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

### <span data-ttu-id="01033-121">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="01033-121">-ServiceName</span></span>
<span data-ttu-id="01033-122">A telepített API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="01033-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="01033-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01033-123">CommonParameters</span></span>
<span data-ttu-id="01033-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="01033-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01033-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="01033-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01033-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="01033-126">INPUTS</span></span>

### <span data-ttu-id="01033-127">System. String</span><span class="sxs-lookup"><span data-stu-id="01033-127">System.String</span></span>

## <span data-ttu-id="01033-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01033-128">OUTPUTS</span></span>

### <span data-ttu-id="01033-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01033-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="01033-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="01033-130">NOTES</span></span>

## <span data-ttu-id="01033-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01033-131">RELATED LINKS</span></span>

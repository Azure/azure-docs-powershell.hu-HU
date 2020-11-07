---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671675"
---
# <span data-ttu-id="bae3c-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bae3c-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="bae3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bae3c-102">SYNOPSIS</span></span>
<span data-ttu-id="bae3c-103">Létrehozza a PsAzureApiManagementContext példányát.</span><span class="sxs-lookup"><span data-stu-id="bae3c-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="bae3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bae3c-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bae3c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bae3c-105">DESCRIPTION</span></span>
<span data-ttu-id="bae3c-106">A **New-AzApiManagementContext** parancsmag a **PsAzureApiManagementContext** példányát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="bae3c-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="bae3c-107">A környezet az API-kezelési szolgáltatás összes parancsmagja esetén használatos.</span><span class="sxs-lookup"><span data-stu-id="bae3c-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="bae3c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bae3c-108">EXAMPLES</span></span>

### <span data-ttu-id="bae3c-109">1. példa: PsApiManagementContext-példány létrehozása</span><span class="sxs-lookup"><span data-stu-id="bae3c-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="bae3c-110">Ez a parancs létrehoz egy **PsApiManagementContext** -példányt.</span><span class="sxs-lookup"><span data-stu-id="bae3c-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="bae3c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bae3c-111">PARAMETERS</span></span>

### <span data-ttu-id="bae3c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bae3c-112">-DefaultProfile</span></span>
<span data-ttu-id="bae3c-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bae3c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bae3c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bae3c-114">-ResourceGroupName</span></span>
<span data-ttu-id="bae3c-115">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt egy API-kezelési szolgáltatás van telepítve.</span><span class="sxs-lookup"><span data-stu-id="bae3c-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="bae3c-116">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="bae3c-116">-ServiceName</span></span>
<span data-ttu-id="bae3c-117">A telepített API-kezelési szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bae3c-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="bae3c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bae3c-118">CommonParameters</span></span>
<span data-ttu-id="bae3c-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bae3c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bae3c-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bae3c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bae3c-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bae3c-121">INPUTS</span></span>

### <span data-ttu-id="bae3c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bae3c-122">System.String</span></span>

## <span data-ttu-id="bae3c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bae3c-123">OUTPUTS</span></span>

### <span data-ttu-id="bae3c-124">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bae3c-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="bae3c-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bae3c-125">NOTES</span></span>

## <span data-ttu-id="bae3c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bae3c-126">RELATED LINKS</span></span>

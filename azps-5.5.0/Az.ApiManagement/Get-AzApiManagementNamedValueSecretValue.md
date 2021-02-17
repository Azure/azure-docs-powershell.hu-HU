---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205727"
---
# <span data-ttu-id="ff7bb-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="ff7bb-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="ff7bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7bb-103">Titkos értéket kap az adott elnevezett értékből.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="ff7bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ff7bb-104">SYNTAX</span></span>

### <span data-ttu-id="ff7bb-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff7bb-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff7bb-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="ff7bb-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff7bb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ff7bb-107">DESCRIPTION</span></span>
<span data-ttu-id="ff7bb-108">Titkos értéket kap az adott elnevezett értékből.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="ff7bb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ff7bb-109">EXAMPLES</span></span>

### <span data-ttu-id="ff7bb-110">1. példa: Névvel megadott érték lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="ff7bb-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="ff7bb-111">Ez a parancs megkapja az elnevezett érték részleteit az elnevezett értéknév alapján.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="ff7bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff7bb-112">PARAMETERS</span></span>

### <span data-ttu-id="ff7bb-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ff7bb-113">-Context</span></span>
<span data-ttu-id="ff7bb-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ff7bb-115">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7bb-116">-DefaultProfile</span></span>
<span data-ttu-id="ff7bb-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff7bb-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="ff7bb-118">-NamedValueId</span></span>
<span data-ttu-id="ff7bb-119">A névvel megadott érték azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-119">Identifier of a the named value.</span></span>
<span data-ttu-id="ff7bb-120">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7bb-121">CommonParameters</span></span>
<span data-ttu-id="ff7bb-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7bb-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff7bb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7bb-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff7bb-124">INPUTS</span></span>

### <span data-ttu-id="ff7bb-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ff7bb-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ff7bb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ff7bb-126">System.String</span></span>

## <span data-ttu-id="ff7bb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff7bb-127">OUTPUTS</span></span>

### <span data-ttu-id="ff7bb-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="ff7bb-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="ff7bb-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ff7bb-129">NOTES</span></span>

## <span data-ttu-id="ff7bb-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff7bb-130">RELATED LINKS</span></span>

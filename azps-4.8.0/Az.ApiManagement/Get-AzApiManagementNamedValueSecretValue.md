---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024966"
---
# <span data-ttu-id="395f3-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="395f3-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="395f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="395f3-102">SYNOPSIS</span></span>
<span data-ttu-id="395f3-103">Az adott névvel ellátott érték titkos értéke lesz.</span><span class="sxs-lookup"><span data-stu-id="395f3-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="395f3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="395f3-104">SYNTAX</span></span>

### <span data-ttu-id="395f3-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="395f3-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="395f3-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="395f3-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="395f3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="395f3-107">DESCRIPTION</span></span>
<span data-ttu-id="395f3-108">Az adott névvel ellátott érték titkos értéke lesz.</span><span class="sxs-lookup"><span data-stu-id="395f3-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="395f3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="395f3-109">EXAMPLES</span></span>

### <span data-ttu-id="395f3-110">Példa 1: elnevezett érték beolvasása név szerint</span><span class="sxs-lookup"><span data-stu-id="395f3-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="395f3-111">Ez a parancs a névvel ellátott érték nevében adja meg az elnevezett érték adatait.</span><span class="sxs-lookup"><span data-stu-id="395f3-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="395f3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="395f3-112">PARAMETERS</span></span>

### <span data-ttu-id="395f3-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="395f3-113">-Context</span></span>
<span data-ttu-id="395f3-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="395f3-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="395f3-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="395f3-115">This parameter is required.</span></span>

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

### <span data-ttu-id="395f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395f3-116">-DefaultProfile</span></span>
<span data-ttu-id="395f3-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="395f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="395f3-118">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="395f3-118">-NamedValueId</span></span>
<span data-ttu-id="395f3-119">A névvel ellátott érték azonosítója</span><span class="sxs-lookup"><span data-stu-id="395f3-119">Identifier of a the named value.</span></span>
<span data-ttu-id="395f3-120">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="395f3-120">This parameter is required.</span></span>

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

### <span data-ttu-id="395f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395f3-121">CommonParameters</span></span>
<span data-ttu-id="395f3-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="395f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395f3-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="395f3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395f3-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="395f3-124">INPUTS</span></span>

### <span data-ttu-id="395f3-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="395f3-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="395f3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="395f3-126">System.String</span></span>

## <span data-ttu-id="395f3-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="395f3-127">OUTPUTS</span></span>

### <span data-ttu-id="395f3-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="395f3-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="395f3-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="395f3-129">NOTES</span></span>

## <span data-ttu-id="395f3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="395f3-130">RELATED LINKS</span></span>

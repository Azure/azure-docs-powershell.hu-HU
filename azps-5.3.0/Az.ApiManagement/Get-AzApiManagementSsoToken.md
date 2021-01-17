---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478914"
---
# <span data-ttu-id="c4aa9-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="c4aa9-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="c4aa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="c4aa9-103">Egy SSO-jogkivonattal egy API felügyeleti szolgáltatás üzembe helyezett felügyeleti portálján található hivatkozást kap.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="c4aa9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4aa9-104">SYNTAX</span></span>

### <span data-ttu-id="c4aa9-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4aa9-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4aa9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c4aa9-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4aa9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4aa9-107">DESCRIPTION</span></span>
<span data-ttu-id="c4aa9-108">A **Get-AzApiManagementSsoToken** parancsmag egy olyan hivatkozást (URL-t) ad vissza, amely egyetlen bejelentkezési (SSO) jogkivonatot tartalmaz egy API management service üzembe helyezett felügyeleti portálján.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="c4aa9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4aa9-109">EXAMPLES</span></span>

### <span data-ttu-id="c4aa9-110">1. példa: API-felügyeleti szolgáltatás SSO-jogkivonatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c4aa9-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="c4aa9-111">Ez a parancs egy API-felügyeleti szolgáltatás SSO-jogkivonatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="c4aa9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4aa9-112">PARAMETERS</span></span>

### <span data-ttu-id="c4aa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4aa9-113">-DefaultProfile</span></span>
<span data-ttu-id="c4aa9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4aa9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4aa9-115">-InputObject</span></span>
<span data-ttu-id="c4aa9-116">A PsApiManagement példánya.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="c4aa9-117">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4aa9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c4aa9-118">-Name</span></span>
<span data-ttu-id="c4aa9-119">Az API Management példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4aa9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4aa9-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4aa9-121">Annak az erőforráscsoportnak a neve, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4aa9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4aa9-122">CommonParameters</span></span>
<span data-ttu-id="c4aa9-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4aa9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4aa9-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4aa9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4aa9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4aa9-125">INPUTS</span></span>

### <span data-ttu-id="c4aa9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c4aa9-126">System.String</span></span>

## <span data-ttu-id="c4aa9-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4aa9-127">OUTPUTS</span></span>

### <span data-ttu-id="c4aa9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c4aa9-128">System.String</span></span>

## <span data-ttu-id="c4aa9-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4aa9-129">NOTES</span></span>

## <span data-ttu-id="c4aa9-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4aa9-130">RELATED LINKS</span></span>

[<span data-ttu-id="c4aa9-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c4aa9-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



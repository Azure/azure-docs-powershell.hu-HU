---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: b4c89a1f0da5e4ce07d9d2174fce031365e09cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932153"
---
# <span data-ttu-id="0249e-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="0249e-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="0249e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0249e-102">SYNOPSIS</span></span>
<span data-ttu-id="0249e-103">Egy felhasználó SSO URL-címét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0249e-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="0249e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0249e-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0249e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0249e-105">DESCRIPTION</span></span>
<span data-ttu-id="0249e-106">A **Get-AzApiManagementUserSsoUrl** parancsmag egyetlen bejelentkezési URL-címet hoz létre a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="0249e-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="0249e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0249e-107">EXAMPLES</span></span>

### <span data-ttu-id="0249e-108">1. példa: Felhasználó SSO URL-címének lekérte</span><span class="sxs-lookup"><span data-stu-id="0249e-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0249e-109">Ez a parancs a felhasználó SSO URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0249e-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="0249e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0249e-110">PARAMETERS</span></span>

### <span data-ttu-id="0249e-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0249e-111">-Context</span></span>
<span data-ttu-id="0249e-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="0249e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0249e-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0249e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0249e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0249e-114">-DefaultProfile</span></span>
<span data-ttu-id="0249e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0249e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0249e-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="0249e-116">-UserId</span></span>
<span data-ttu-id="0249e-117">Felhasználóazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0249e-117">Specifies a user ID.</span></span>
<span data-ttu-id="0249e-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="0249e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0249e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0249e-119">CommonParameters</span></span>
<span data-ttu-id="0249e-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0249e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0249e-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0249e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0249e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0249e-122">INPUTS</span></span>

### <span data-ttu-id="0249e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0249e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0249e-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0249e-124">System.String</span></span>

## <span data-ttu-id="0249e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0249e-125">OUTPUTS</span></span>

### <span data-ttu-id="0249e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0249e-126">System.String</span></span>

## <span data-ttu-id="0249e-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0249e-127">NOTES</span></span>

## <span data-ttu-id="0249e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0249e-128">RELATED LINKS</span></span>

[<span data-ttu-id="0249e-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0249e-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)



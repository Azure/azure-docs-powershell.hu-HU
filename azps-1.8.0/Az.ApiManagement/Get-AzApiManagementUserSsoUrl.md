---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: 2a7a4d602b8e316377496af8ccb9c119338a5c99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665660"
---
# <span data-ttu-id="0e15e-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="0e15e-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="0e15e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e15e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e15e-103">Egy felhasználó bejelentkezési URL-címét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="0e15e-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="0e15e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e15e-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e15e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e15e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e15e-106">A **Get-AzApiManagementUserSsoUrl** parancsmag egyszeri bejelentkezési (SSO) URL-címet hoz létre a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="0e15e-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="0e15e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0e15e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e15e-108">Példa 1: felhasználó bejelentkezési URL-címének beszerzése</span><span class="sxs-lookup"><span data-stu-id="0e15e-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0e15e-109">Ez a parancs a felhasználó bejelentkezési URL-címét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0e15e-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="0e15e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e15e-110">PARAMETERS</span></span>

### <span data-ttu-id="0e15e-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0e15e-111">-Context</span></span>
<span data-ttu-id="0e15e-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0e15e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="0e15e-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="0e15e-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e15e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e15e-114">-DefaultProfile</span></span>
<span data-ttu-id="0e15e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e15e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e15e-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="0e15e-116">-UserId</span></span>
<span data-ttu-id="0e15e-117">Egy felhasználói azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="0e15e-117">Specifies a user ID.</span></span>
<span data-ttu-id="0e15e-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="0e15e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0e15e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e15e-119">CommonParameters</span></span>
<span data-ttu-id="0e15e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e15e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e15e-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e15e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e15e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e15e-122">INPUTS</span></span>

### <span data-ttu-id="0e15e-123">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0e15e-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0e15e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0e15e-124">System.String</span></span>

## <span data-ttu-id="0e15e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e15e-125">OUTPUTS</span></span>

### <span data-ttu-id="0e15e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0e15e-126">System.String</span></span>

## <span data-ttu-id="0e15e-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e15e-127">NOTES</span></span>

## <span data-ttu-id="0e15e-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e15e-128">RELATED LINKS</span></span>

[<span data-ttu-id="0e15e-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0e15e-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)



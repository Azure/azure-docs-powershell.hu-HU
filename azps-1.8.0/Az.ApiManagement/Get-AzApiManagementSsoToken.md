---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665666"
---
# <span data-ttu-id="514d5-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="514d5-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="514d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="514d5-102">SYNOPSIS</span></span>
<span data-ttu-id="514d5-103">Egy, az API-menedzsment szolgáltatással rendelkező, telepített felügyeleti webhelyre mutató, SSO-tokent tartalmazó hivatkozást kap.</span><span class="sxs-lookup"><span data-stu-id="514d5-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="514d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="514d5-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="514d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="514d5-105">DESCRIPTION</span></span>
<span data-ttu-id="514d5-106">A **Get-AzApiManagementSsoToken** parancsmag egy olyan hivatkozást (URL-címet) ad eredményül, amely egyszeri bejelentkezési (SSO) jogkivonatot tartalmaz egy API-kezelési szolgáltatás telepített felügyeleti portálján.</span><span class="sxs-lookup"><span data-stu-id="514d5-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="514d5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="514d5-107">EXAMPLES</span></span>

### <span data-ttu-id="514d5-108">Példa 1: az API-menedzsment szolgáltatás egyszeri bejelentkezési jogkivonatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="514d5-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="514d5-109">Ez a parancs egy API-kezelési szolgáltatás SSO-jogkivonatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="514d5-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="514d5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="514d5-110">PARAMETERS</span></span>

### <span data-ttu-id="514d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="514d5-111">-DefaultProfile</span></span>
<span data-ttu-id="514d5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="514d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="514d5-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="514d5-113">-Name</span></span>
<span data-ttu-id="514d5-114">Az API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="514d5-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="514d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="514d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="514d5-116">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="514d5-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="514d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514d5-117">CommonParameters</span></span>
<span data-ttu-id="514d5-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="514d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514d5-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="514d5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514d5-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="514d5-120">INPUTS</span></span>

### <span data-ttu-id="514d5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="514d5-121">System.String</span></span>

## <span data-ttu-id="514d5-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="514d5-122">OUTPUTS</span></span>

### <span data-ttu-id="514d5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="514d5-123">System.String</span></span>

## <span data-ttu-id="514d5-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="514d5-124">NOTES</span></span>

## <span data-ttu-id="514d5-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="514d5-125">RELATED LINKS</span></span>

[<span data-ttu-id="514d5-126">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="514d5-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



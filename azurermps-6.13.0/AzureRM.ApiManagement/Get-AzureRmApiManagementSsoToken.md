---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: e0bce4f579b2000bc970e35ceb03da03fdffb211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492089"
---
# <span data-ttu-id="45cdc-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="45cdc-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="45cdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="45cdc-103">Egy, az API-menedzsment szolgáltatással rendelkező, telepített felügyeleti webhelyre mutató, SSO-tokent tartalmazó hivatkozást kap.</span><span class="sxs-lookup"><span data-stu-id="45cdc-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45cdc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45cdc-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45cdc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="45cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="45cdc-106">A **Get-AzureRmApiManagementSsoToken** parancsmag egy olyan hivatkozást (URL-címet) ad eredményül, amely egyszeri bejelentkezési (SSO) jogkivonatot tartalmaz egy API-kezelési szolgáltatás telepített felügyeleti portálján.</span><span class="sxs-lookup"><span data-stu-id="45cdc-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="45cdc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="45cdc-107">EXAMPLES</span></span>

### <span data-ttu-id="45cdc-108">Példa 1: az API-menedzsment szolgáltatás egyszeri bejelentkezési jogkivonatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="45cdc-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="45cdc-109">Ez a parancs egy API-kezelési szolgáltatás SSO-jogkivonatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="45cdc-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="45cdc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45cdc-110">PARAMETERS</span></span>

### <span data-ttu-id="45cdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45cdc-111">-DefaultProfile</span></span>
<span data-ttu-id="45cdc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45cdc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45cdc-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45cdc-113">-Name</span></span>
<span data-ttu-id="45cdc-114">Az API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45cdc-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="45cdc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45cdc-115">-ResourceGroupName</span></span>
<span data-ttu-id="45cdc-116">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="45cdc-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="45cdc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45cdc-117">CommonParameters</span></span>
<span data-ttu-id="45cdc-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45cdc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45cdc-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45cdc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45cdc-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45cdc-120">INPUTS</span></span>

### <span data-ttu-id="45cdc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="45cdc-121">System.String</span></span>

## <span data-ttu-id="45cdc-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45cdc-122">OUTPUTS</span></span>

### <span data-ttu-id="45cdc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="45cdc-123">System.String</span></span>

## <span data-ttu-id="45cdc-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45cdc-124">NOTES</span></span>

## <span data-ttu-id="45cdc-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45cdc-125">RELATED LINKS</span></span>

[<span data-ttu-id="45cdc-126">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="45cdc-126">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018012"
---
# <span data-ttu-id="c62a9-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="c62a9-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="c62a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c62a9-102">SYNOPSIS</span></span>
<span data-ttu-id="c62a9-103">Egy, az API-menedzsment szolgáltatással rendelkező, telepített felügyeleti webhelyre mutató, SSO-tokent tartalmazó hivatkozást kap.</span><span class="sxs-lookup"><span data-stu-id="c62a9-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="c62a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c62a9-104">SYNTAX</span></span>

### <span data-ttu-id="c62a9-105">ExpandedParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c62a9-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c62a9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c62a9-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c62a9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c62a9-107">DESCRIPTION</span></span>
<span data-ttu-id="c62a9-108">A **Get-AzApiManagementSsoToken** parancsmag egy olyan hivatkozást (URL-címet) ad eredményül, amely egyszeri bejelentkezési (SSO) jogkivonatot tartalmaz egy API-kezelési szolgáltatás telepített felügyeleti portálján.</span><span class="sxs-lookup"><span data-stu-id="c62a9-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="c62a9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c62a9-109">EXAMPLES</span></span>

### <span data-ttu-id="c62a9-110">Példa 1: az API-menedzsment szolgáltatás egyszeri bejelentkezési jogkivonatának beszerzése</span><span class="sxs-lookup"><span data-stu-id="c62a9-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="c62a9-111">Ez a parancs egy API-kezelési szolgáltatás SSO-jogkivonatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c62a9-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="c62a9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c62a9-112">PARAMETERS</span></span>

### <span data-ttu-id="c62a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62a9-113">-DefaultProfile</span></span>
<span data-ttu-id="c62a9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c62a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c62a9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c62a9-115">-InputObject</span></span>
<span data-ttu-id="c62a9-116">A PsApiManagement példánya.</span><span class="sxs-lookup"><span data-stu-id="c62a9-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="c62a9-117">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="c62a9-117">This parameter is required.</span></span>

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

### <span data-ttu-id="c62a9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c62a9-118">-Name</span></span>
<span data-ttu-id="c62a9-119">Az API-kezelési példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c62a9-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="c62a9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62a9-120">-ResourceGroupName</span></span>
<span data-ttu-id="c62a9-121">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.</span><span class="sxs-lookup"><span data-stu-id="c62a9-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="c62a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62a9-122">CommonParameters</span></span>
<span data-ttu-id="c62a9-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c62a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62a9-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c62a9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62a9-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c62a9-125">INPUTS</span></span>

### <span data-ttu-id="c62a9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c62a9-126">System.String</span></span>

## <span data-ttu-id="c62a9-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c62a9-127">OUTPUTS</span></span>

### <span data-ttu-id="c62a9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c62a9-128">System.String</span></span>

## <span data-ttu-id="c62a9-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c62a9-129">NOTES</span></span>

## <span data-ttu-id="c62a9-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c62a9-130">RELATED LINKS</span></span>

[<span data-ttu-id="c62a9-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c62a9-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



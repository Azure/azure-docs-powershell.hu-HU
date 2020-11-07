---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 2d7a7d61d5a29113f9b0e40340ae6b13b599115f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666782"
---
# <span data-ttu-id="2d6e8-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="2d6e8-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="2d6e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6e8-103">Új példány létrehozása DataMigration Azure ActiveDirectory Application details.</span><span class="sxs-lookup"><span data-stu-id="2d6e8-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="2d6e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d6e8-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d6e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d6e8-105">DESCRIPTION</span></span>
<span data-ttu-id="2d6e8-106">Új példány létrehozása DataMigration Azure ActiveDirectory Application details.</span><span class="sxs-lookup"><span data-stu-id="2d6e8-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="2d6e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d6e8-107">EXAMPLES</span></span>

### <span data-ttu-id="2d6e8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2d6e8-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="2d6e8-109">ApplicationId: "a AppId/Service Principal id" AppKey: System. Security. SecureString bérlői azonosító megkeresése: "bérlői azonosító"</span><span class="sxs-lookup"><span data-stu-id="2d6e8-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="2d6e8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d6e8-110">PARAMETERS</span></span>

### <span data-ttu-id="2d6e8-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="2d6e8-111">-AppKey</span></span>
<span data-ttu-id="2d6e8-112">Azure Active Directory-kulcs</span><span class="sxs-lookup"><span data-stu-id="2d6e8-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6e8-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2d6e8-113">-ApplicationId</span></span>
<span data-ttu-id="2d6e8-114">Azure Active Directory-alkalmazás azonosítója</span><span class="sxs-lookup"><span data-stu-id="2d6e8-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d6e8-115">-DefaultProfile</span></span>
<span data-ttu-id="2d6e8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d6e8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d6e8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6e8-117">CommonParameters</span></span>
<span data-ttu-id="2d6e8-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d6e8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2d6e8-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d6e8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6e8-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d6e8-120">INPUTS</span></span>

### <span data-ttu-id="2d6e8-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="2d6e8-121">None</span></span>

## <span data-ttu-id="2d6e8-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d6e8-122">OUTPUTS</span></span>

### <span data-ttu-id="2d6e8-123">Microsoft. Azure. Command. DataMigration. models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="2d6e8-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="2d6e8-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d6e8-124">NOTES</span></span>

## <span data-ttu-id="2d6e8-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d6e8-125">RELATED LINKS</span></span>

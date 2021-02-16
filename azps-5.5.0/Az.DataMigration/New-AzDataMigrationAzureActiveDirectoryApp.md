---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161850"
---
# <span data-ttu-id="dbc9c-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="dbc9c-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="dbc9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc9c-103">Új példány létrehozása: DataMigration Azure ActiveDirectory Application details.</span><span class="sxs-lookup"><span data-stu-id="dbc9c-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="dbc9c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="dbc9c-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbc9c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="dbc9c-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc9c-106">Új példány létrehozása: DataMigration Azure ActiveDirectory Application details.</span><span class="sxs-lookup"><span data-stu-id="dbc9c-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="dbc9c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="dbc9c-107">EXAMPLES</span></span>

### <span data-ttu-id="dbc9c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="dbc9c-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="dbc9c-109">ApplicationId: "Az Ön AppId/Service Principal Id here" AppKey: System.Security.SecureString TenantId: "Tenant Id"</span><span class="sxs-lookup"><span data-stu-id="dbc9c-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="dbc9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbc9c-110">PARAMETERS</span></span>

### <span data-ttu-id="dbc9c-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="dbc9c-111">-AppKey</span></span>
<span data-ttu-id="dbc9c-112">Azure Active Directory-kulcs</span><span class="sxs-lookup"><span data-stu-id="dbc9c-112">Azure Active Directory Key</span></span>

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

### <span data-ttu-id="dbc9c-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dbc9c-113">-ApplicationId</span></span>
<span data-ttu-id="dbc9c-114">Azure Active Directory-alkalmazásazonosító</span><span class="sxs-lookup"><span data-stu-id="dbc9c-114">Azure Active Directory Application Id</span></span>

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

### <span data-ttu-id="dbc9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc9c-115">-DefaultProfile</span></span>
<span data-ttu-id="dbc9c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dbc9c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc9c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc9c-117">CommonParameters</span></span>
<span data-ttu-id="dbc9c-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc9c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dbc9c-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc9c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc9c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbc9c-120">INPUTS</span></span>

### <span data-ttu-id="dbc9c-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="dbc9c-121">None</span></span>

## <span data-ttu-id="dbc9c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dbc9c-122">OUTPUTS</span></span>

### <span data-ttu-id="dbc9c-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="dbc9c-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="dbc9c-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="dbc9c-124">NOTES</span></span>

## <span data-ttu-id="dbc9c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dbc9c-125">RELATED LINKS</span></span>

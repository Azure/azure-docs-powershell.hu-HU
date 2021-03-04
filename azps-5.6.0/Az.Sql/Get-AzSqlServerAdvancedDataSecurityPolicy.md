---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 372951b708d34c44706f981424b7ace39efff2b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929706"
---
# <span data-ttu-id="521ff-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="521ff-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="521ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="521ff-102">SYNOPSIS</span></span>
<span data-ttu-id="521ff-103">A kiszolgáló speciális adatbiztonsági házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="521ff-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="521ff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="521ff-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="521ff-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="521ff-105">DESCRIPTION</span></span>
<span data-ttu-id="521ff-106">A **Get-AzSqlServerAdvancedDataSecurityPolicy** parancsmag beolvassa egy kiszolgáló speciális adatbiztonsági házirendjét.</span><span class="sxs-lookup"><span data-stu-id="521ff-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="521ff-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="521ff-107">EXAMPLES</span></span>

### <span data-ttu-id="521ff-108">1. példa: Kiszolgáló speciális adatbiztonságának lekérte</span><span class="sxs-lookup"><span data-stu-id="521ff-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="521ff-109">2. példa: Kiszolgáló speciális adatbiztonságot kap a kiszolgálóerőforrástól</span><span class="sxs-lookup"><span data-stu-id="521ff-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="521ff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="521ff-110">PARAMETERS</span></span>

### <span data-ttu-id="521ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521ff-111">-DefaultProfile</span></span>
<span data-ttu-id="521ff-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="521ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="521ff-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="521ff-113">-InputObject</span></span>
<span data-ttu-id="521ff-114">The server object to use with Advanced Data Security policy operation</span><span class="sxs-lookup"><span data-stu-id="521ff-114">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="521ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="521ff-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="521ff-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521ff-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="521ff-117">-ServerName</span></span>
<span data-ttu-id="521ff-118">SQL-adatbázis-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="521ff-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="521ff-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521ff-119">CommonParameters</span></span>
<span data-ttu-id="521ff-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="521ff-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521ff-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="521ff-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521ff-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="521ff-122">INPUTS</span></span>

### <span data-ttu-id="521ff-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="521ff-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="521ff-124">System.String</span><span class="sxs-lookup"><span data-stu-id="521ff-124">System.String</span></span>

## <span data-ttu-id="521ff-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="521ff-125">OUTPUTS</span></span>

### <span data-ttu-id="521ff-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="521ff-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="521ff-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="521ff-127">NOTES</span></span>

## <span data-ttu-id="521ff-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="521ff-128">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 14075af7cd18b27965de66c738edfaf0ffe64fd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013071"
---
# <span data-ttu-id="b0f0d-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="b0f0d-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="b0f0d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f0d-103">Speciális adatbiztonsági házirendet kap egy kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="b0f0d-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="b0f0d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0f0d-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0f0d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="b0f0d-106">A **Get-AzSqlServerAdvancedDataSecurityPolicy** parancsmag a kiszolgáló speciális adatbiztonsági házirendjének lekérdezését kéri.</span><span class="sxs-lookup"><span data-stu-id="b0f0d-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="b0f0d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b0f0d-107">EXAMPLES</span></span>

### <span data-ttu-id="b0f0d-108">Példa 1 – a kiszolgáló speciális adatbiztonsága</span><span class="sxs-lookup"><span data-stu-id="b0f0d-108">Example 1 - Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="b0f0d-109">Példa: a Server Advanced Data Security a kiszolgáló-erőforrástól kapja</span><span class="sxs-lookup"><span data-stu-id="b0f0d-109">Example 2 - Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="b0f0d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0f0d-110">PARAMETERS</span></span>

### <span data-ttu-id="b0f0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f0d-111">-DefaultProfile</span></span>
<span data-ttu-id="b0f0d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0f0d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f0d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0f0d-113">-InputObject</span></span>
<span data-ttu-id="b0f0d-114">A kiszolgálói objektum, amely a speciális adatbiztonsági házirend-művelethez van használatban</span><span class="sxs-lookup"><span data-stu-id="b0f0d-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="b0f0d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0f0d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b0f0d-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b0f0d-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="b0f0d-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b0f0d-117">-ServerName</span></span>
<span data-ttu-id="b0f0d-118">SQL-adatbázis kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="b0f0d-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="b0f0d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f0d-119">CommonParameters</span></span>
<span data-ttu-id="b0f0d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0f0d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f0d-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b0f0d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f0d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0f0d-122">INPUTS</span></span>

### <span data-ttu-id="b0f0d-123">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b0f0d-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="b0f0d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b0f0d-124">System.String</span></span>

## <span data-ttu-id="b0f0d-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0f0d-125">OUTPUTS</span></span>

### <span data-ttu-id="b0f0d-126">Microsoft. Azure. Command. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b0f0d-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b0f0d-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0f0d-127">NOTES</span></span>

## <span data-ttu-id="b0f0d-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0f0d-128">RELATED LINKS</span></span>

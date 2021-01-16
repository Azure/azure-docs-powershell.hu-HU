---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476657"
---
# <span data-ttu-id="c6f13-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="c6f13-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="c6f13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f13-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f13-103">Egy adatbázis-kiszolgáló rendszer-helyreállítási konfigurációjának tevékenységét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c6f13-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="c6f13-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c6f13-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6f13-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c6f13-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f13-106">A **Get-AzSqlServerDisasterRecoveryConfigurationActivity** parancsmag tevékenységet kap egy SQL-adatbázis-kiszolgáló rendszer-helyreállítási konfigurációjában.</span><span class="sxs-lookup"><span data-stu-id="c6f13-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="c6f13-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c6f13-107">EXAMPLES</span></span>

## <span data-ttu-id="c6f13-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6f13-108">PARAMETERS</span></span>

### <span data-ttu-id="c6f13-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f13-109">-DefaultProfile</span></span>
<span data-ttu-id="c6f13-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c6f13-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6f13-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c6f13-111">-OperationId</span></span>
<span data-ttu-id="c6f13-112">A műveletazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6f13-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f13-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f13-113">-ResourceGroupName</span></span>
<span data-ttu-id="c6f13-114">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6f13-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c6f13-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c6f13-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="c6f13-116">A kiszolgálórendszer helyreállítási konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6f13-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="c6f13-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6f13-117">-ServerName</span></span>
<span data-ttu-id="c6f13-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c6f13-118">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f13-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6f13-119">-Confirm</span></span>
<span data-ttu-id="c6f13-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c6f13-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f13-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f13-121">-WhatIf</span></span>
<span data-ttu-id="c6f13-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c6f13-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6f13-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c6f13-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f13-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f13-124">CommonParameters</span></span>
<span data-ttu-id="c6f13-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6f13-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f13-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6f13-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f13-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6f13-127">INPUTS</span></span>

### <span data-ttu-id="c6f13-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c6f13-128">System.String</span></span>

### <span data-ttu-id="c6f13-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c6f13-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c6f13-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c6f13-130">OUTPUTS</span></span>

### <span data-ttu-id="c6f13-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="c6f13-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="c6f13-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c6f13-132">NOTES</span></span>

## <span data-ttu-id="c6f13-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c6f13-133">RELATED LINKS</span></span>

[<span data-ttu-id="c6f13-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="c6f13-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

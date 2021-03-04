---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 68e81a7f51ca385d5671698ad8624f523ae98c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923929"
---
# <span data-ttu-id="6de3f-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="6de3f-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="6de3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6de3f-102">SYNOPSIS</span></span>
<span data-ttu-id="6de3f-103">Egy adatbázis-kiszolgálói rendszer helyreállítási konfigurációjának tevékenységét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6de3f-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="6de3f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6de3f-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de3f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6de3f-105">DESCRIPTION</span></span>
<span data-ttu-id="6de3f-106">A **Get-AzSqlServerDisasterRecoveryConfigurationActivity** parancsmag egy SQL-adatbázis-kiszolgálói rendszer helyreállítási konfigurációjában kap tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="6de3f-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="6de3f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6de3f-107">EXAMPLES</span></span>

## <span data-ttu-id="6de3f-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6de3f-108">PARAMETERS</span></span>

### <span data-ttu-id="6de3f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de3f-109">-DefaultProfile</span></span>
<span data-ttu-id="6de3f-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6de3f-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6de3f-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6de3f-111">-OperationId</span></span>
<span data-ttu-id="6de3f-112">A műveletazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="6de3f-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="6de3f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de3f-113">-ResourceGroupName</span></span>
<span data-ttu-id="6de3f-114">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6de3f-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6de3f-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6de3f-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="6de3f-116">A kiszolgálórendszer helyreállítási konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6de3f-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="6de3f-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6de3f-117">-ServerName</span></span>
<span data-ttu-id="6de3f-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6de3f-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6de3f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6de3f-119">-Confirm</span></span>
<span data-ttu-id="6de3f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6de3f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de3f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de3f-121">-WhatIf</span></span>
<span data-ttu-id="6de3f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6de3f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6de3f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6de3f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de3f-124">CommonParameters</span></span>
<span data-ttu-id="6de3f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de3f-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6de3f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de3f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6de3f-127">INPUTS</span></span>

### <span data-ttu-id="6de3f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6de3f-128">System.String</span></span>

### <span data-ttu-id="6de3f-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6de3f-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6de3f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6de3f-130">OUTPUTS</span></span>

### <span data-ttu-id="6de3f-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="6de3f-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="6de3f-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6de3f-132">NOTES</span></span>

## <span data-ttu-id="6de3f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6de3f-133">RELATED LINKS</span></span>

[<span data-ttu-id="6de3f-134">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="6de3f-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

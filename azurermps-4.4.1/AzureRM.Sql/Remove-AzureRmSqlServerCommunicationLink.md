---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 63bfce9b6f0d6aaa97fede65d8c96ac9079be349
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680462"
---
# <span data-ttu-id="86ebb-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="86ebb-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="86ebb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="86ebb-103">Két kiszolgáló közötti rugalmas adatbázis-tranzakciókat tartalmazó kommunikációs hivatkozás törlése</span><span class="sxs-lookup"><span data-stu-id="86ebb-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ebb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86ebb-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86ebb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86ebb-105">DESCRIPTION</span></span>
<span data-ttu-id="86ebb-106">A **Remove-AzureRmSqlServerCommunicationLink** parancsmagja a kiszolgálók közötti kommunikációs hivatkozást törli az Azure SQL-adatbázisokban található rugalmas adatbázis-tranzakciókban.</span><span class="sxs-lookup"><span data-stu-id="86ebb-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="86ebb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="86ebb-107">EXAMPLES</span></span>

### <span data-ttu-id="86ebb-108">Példa 1: kommunikációs hivatkozás törlése</span><span class="sxs-lookup"><span data-stu-id="86ebb-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="86ebb-109">Ez a parancs törli a ContosoServer17 nevű Link01-kiszolgálóról származó kapcsolati hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="86ebb-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="86ebb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86ebb-110">PARAMETERS</span></span>

### <span data-ttu-id="86ebb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="86ebb-111">-Force</span></span>
<span data-ttu-id="86ebb-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="86ebb-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ebb-113">-LinkName</span><span class="sxs-lookup"><span data-stu-id="86ebb-113">-LinkName</span></span>
<span data-ttu-id="86ebb-114">Annak a kiszolgáló-kommunikációs hivatkozásnak a nevét adja meg, amelyre a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="86ebb-114">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ebb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ebb-115">-ResourceGroupName</span></span>
<span data-ttu-id="86ebb-116">Annak az erőforráscsoport a neve, amelyhez a *kiszolgálónév* paraméter által megadott kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="86ebb-116">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="86ebb-117">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="86ebb-117">-ServerName</span></span>
<span data-ttu-id="86ebb-118">A kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86ebb-118">Specifies the name of a server.</span></span>
<span data-ttu-id="86ebb-119">Ebben a kiszolgálón található a parancsmag által törölt kommunikációs hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="86ebb-119">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="86ebb-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86ebb-120">-Confirm</span></span>
<span data-ttu-id="86ebb-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86ebb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ebb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ebb-122">-WhatIf</span></span>
<span data-ttu-id="86ebb-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86ebb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ebb-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86ebb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ebb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ebb-125">-DefaultProfile</span></span>
<span data-ttu-id="86ebb-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86ebb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86ebb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ebb-127">CommonParameters</span></span>
<span data-ttu-id="86ebb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86ebb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ebb-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ebb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ebb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86ebb-130">INPUTS</span></span>

## <span data-ttu-id="86ebb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86ebb-131">OUTPUTS</span></span>

### <span data-ttu-id="86ebb-132">Microsoft. Azure. Command. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="86ebb-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="86ebb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86ebb-133">NOTES</span></span>
* <span data-ttu-id="86ebb-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, SQL, adatbázis, MSSQL</span><span class="sxs-lookup"><span data-stu-id="86ebb-134">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="86ebb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86ebb-135">RELATED LINKS</span></span>

[<span data-ttu-id="86ebb-136">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="86ebb-136">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="86ebb-137">Új – AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="86ebb-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="86ebb-138">SQL-adatbázis dokumentációja</span><span class="sxs-lookup"><span data-stu-id="86ebb-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

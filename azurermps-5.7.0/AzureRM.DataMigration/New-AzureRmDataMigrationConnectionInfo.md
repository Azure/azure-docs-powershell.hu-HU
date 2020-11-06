---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493793"
---
# <span data-ttu-id="66a16-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="66a16-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="66a16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66a16-102">SYNOPSIS</span></span>
<span data-ttu-id="66a16-103">Új kapcsolati adatobjektumot hoz létre a kiszolgáló típusa és a kapcsolat neve mezőben.</span><span class="sxs-lookup"><span data-stu-id="66a16-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66a16-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="66a16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66a16-105">DESCRIPTION</span></span>
<span data-ttu-id="66a16-106">A New-AzureRmDataMigrationConnectionInfo parancsmag létrehoz egy új kapcsolatot a kapcsolati adatok objektummal, amely a kapcsolat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="66a16-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="66a16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66a16-107">EXAMPLES</span></span>

### <span data-ttu-id="66a16-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="66a16-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="66a16-109">Az előző példa létrehoz egy új kapcsolati adatkapcsolatú objektumot, amely az SQL ServerType paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="66a16-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="66a16-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66a16-110">PARAMETERS</span></span>

### <span data-ttu-id="66a16-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66a16-111">-Confirm</span></span>
<span data-ttu-id="66a16-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66a16-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="66a16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a16-113">-DefaultProfile</span></span>
<span data-ttu-id="66a16-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66a16-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a16-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="66a16-115">-ServerType</span></span>
<span data-ttu-id="66a16-116">A kiszolgálóhoz való csatlakozáshoz kapcsolódó Fájltípus leírása.</span><span class="sxs-lookup"><span data-stu-id="66a16-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="66a16-117">A jelenleg támogatott értékek az SQL Server és az SQL Azure-adatbázis SQLDB.</span><span class="sxs-lookup"><span data-stu-id="66a16-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="66a16-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="66a16-118">-AuthType</span></span>
<span data-ttu-id="66a16-119">A kapcsolathoz használandó hitelesítési típus.</span><span class="sxs-lookup"><span data-stu-id="66a16-119">Authentication type to use for connection.</span></span> <span data-ttu-id="66a16-120">A lehetséges értékek a SqlAuthentication és a WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="66a16-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a16-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="66a16-121">-DataSource</span></span>
<span data-ttu-id="66a16-122">Csatlakozás a kiszolgáló address\name.</span><span class="sxs-lookup"><span data-stu-id="66a16-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a16-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="66a16-123">-TrustServerCertificate</span></span>
<span data-ttu-id="66a16-124">Logikai érték, amely biztosítja, hogy a titkosítás végbemegy.</span><span class="sxs-lookup"><span data-stu-id="66a16-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a16-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a16-125">-WhatIf</span></span>
<span data-ttu-id="66a16-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66a16-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66a16-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66a16-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```





## <span data-ttu-id="66a16-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66a16-128">INPUTS</span></span>

### <span data-ttu-id="66a16-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="66a16-129">None</span></span>


## <span data-ttu-id="66a16-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66a16-130">OUTPUTS</span></span>

### <span data-ttu-id="66a16-131">Microsoft. Azure. Management. DataMigration. models. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="66a16-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="66a16-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66a16-132">NOTES</span></span>

## <span data-ttu-id="66a16-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66a16-133">RELATED LINKS</span></span>


---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015970"
---
# <span data-ttu-id="e8700-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="e8700-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="e8700-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8700-102">SYNOPSIS</span></span>
<span data-ttu-id="e8700-103">Kiszolgáló-kapcsolati környezetet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e8700-103">Creates a server connection context.</span></span>

## <span data-ttu-id="e8700-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8700-104">SYNTAX</span></span>

### <span data-ttu-id="e8700-105">ByServerNameWithSqlAuth (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8700-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8700-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="e8700-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8700-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="e8700-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8700-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="e8700-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e8700-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="e8700-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e8700-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8700-110">DESCRIPTION</span></span>
<span data-ttu-id="e8700-111">A **New-AzureSqlDatabaseServerContext** parancsmag az Azure SQL Database Server kapcsolati környezetét hozza létre.</span><span class="sxs-lookup"><span data-stu-id="e8700-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="e8700-112">SQL Server-hitelesítéssel kapcsolati környezetet hozhat létre egy SQL-adatbázis-kiszolgálóhoz a megadott hitelesítő adatokkal.</span><span class="sxs-lookup"><span data-stu-id="e8700-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="e8700-113">Az SQL-adatbázis kiszolgálóját név szerint is megadhatja a teljesen minősített név vagy URL-cím alapján.</span><span class="sxs-lookup"><span data-stu-id="e8700-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="e8700-114">A hitelesítő adatok megadásához használja a Get-Credential parancsmagot, amely a Felhasználónév és a jelszó megadását kéri.</span><span class="sxs-lookup"><span data-stu-id="e8700-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="e8700-115">Használja a **New-AzureSqlDatabaseServerContext** parancsmagot tanúsítvány-alapú hitelesítéssel a megadott SQL-adatbázis-kiszolgálóhoz való kapcsolódási környezet létrehozásához a megadott Azure-előfizetési adatok használatával.</span><span class="sxs-lookup"><span data-stu-id="e8700-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="e8700-116">Az SQL-adatbázis kiszolgálóját név vagy a teljesen minősített név szerint is megadhatja.</span><span class="sxs-lookup"><span data-stu-id="e8700-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="e8700-117">Az előfizetési adattípusokat paraméterként adhatja meg, vagy az aktuális Azure-előfizetésből beolvashatja.</span><span class="sxs-lookup"><span data-stu-id="e8700-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="e8700-118">Az https://msdn.microsoft.com/library/windowsazure/jj152833.aspx aktuális Azure-előfizetés kiválasztásához használja a Select-AzureSubscription parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e8700-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="e8700-119">Példák</span><span class="sxs-lookup"><span data-stu-id="e8700-119">EXAMPLES</span></span>

### <span data-ttu-id="e8700-120">Példa 1: környezet létrehozása SQL Server-hitelesítés használatával</span><span class="sxs-lookup"><span data-stu-id="e8700-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="e8700-121">Ez a példa az SQL Server-hitelesítést használja.</span><span class="sxs-lookup"><span data-stu-id="e8700-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="e8700-122">Az első parancs kéri a kiszolgáló-rendszergazdai hitelesítő adatok megadását, és a hitelesítő adatokat a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e8700-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="e8700-123">A második parancs a lpqd0zbr8y nevű SQL adatbázis-kiszolgálóhoz csatlakozik a $Credential használatával.</span><span class="sxs-lookup"><span data-stu-id="e8700-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="e8700-124">A végleges parancs létrehoz egy Database17 nevű adatbázist a kiszolgálón, amely az $Context környezet részét képezi.</span><span class="sxs-lookup"><span data-stu-id="e8700-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="e8700-125">2. példa: környezet létrehozása tanúsítvány-alapú hitelesítés használatával</span><span class="sxs-lookup"><span data-stu-id="e8700-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="e8700-126">Ez a példa a tanúsítványon alapuló hitelesítést használja.</span><span class="sxs-lookup"><span data-stu-id="e8700-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="e8700-127">Az első két parancs az értékekhez rendeli az $SubscriptionId és $Thumbprint változókat.</span><span class="sxs-lookup"><span data-stu-id="e8700-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="e8700-128">A harmadik parancs a $Thumbprint ujjlenyomatával azonosított tanúsítványt kapja, és a $Certificate tárolja.</span><span class="sxs-lookup"><span data-stu-id="e8700-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="e8700-129">A negyedik parancs beállítja a Subscription07 előfizetést, és az ötödik parancs kiválasztja az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="e8700-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="e8700-130">A végleges parancs létrehoz egy környezetet a lpqd0zbr8y nevű kiszolgálóhoz tartozó jelenlegi előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e8700-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="e8700-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8700-131">PARAMETERS</span></span>

### <span data-ttu-id="e8700-132">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="e8700-132">-Credential</span></span>
<span data-ttu-id="e8700-133">Megadja azt a hitelesítőadat-objektumot, amely SQL Server-hitelesítést nyújt Önnek a kiszolgáló eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="e8700-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8700-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="e8700-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="e8700-135">Az Azure SQL Server-kiszolgáló teljes tartománynevét (FQDN) tartalmazó nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8700-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="e8700-136">Például Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="e8700-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8700-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="e8700-137">-ManageUrl</span></span>
<span data-ttu-id="e8700-138">Megadja, hogy a parancsmag milyen URL-címet használ az Azure SQL DatabaseManagement-portál eléréséhez a kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="e8700-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8700-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="e8700-139">-Profile</span></span>
<span data-ttu-id="e8700-140">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e8700-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e8700-141">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e8700-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8700-142">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e8700-142">-ServerName</span></span>
<span data-ttu-id="e8700-143">Az adatbázis-kiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8700-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8700-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e8700-144">-SubscriptionName</span></span>
<span data-ttu-id="e8700-145">Megadja annak az Azure-előfizetésnek a nevét, amelyet a parancsmag a kapcsolati környezet létrehozásához használ.</span><span class="sxs-lookup"><span data-stu-id="e8700-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="e8700-146">Ha nem ad meg értéket ehhez a paraméterhez, a parancsmag az aktuális előfizetést használja.</span><span class="sxs-lookup"><span data-stu-id="e8700-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="e8700-147">Az aktuális előfizetés módosításához futtassa az Select-AzureSubscription parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e8700-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8700-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="e8700-148">-UseSubscription</span></span>
<span data-ttu-id="e8700-149">Jelzi, hogy ez a parancsmag Azure-előfizetést használ a kapcsolati környezet létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="e8700-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8700-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8700-150">CommonParameters</span></span>
<span data-ttu-id="e8700-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8700-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8700-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8700-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8700-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8700-153">INPUTS</span></span>

## <span data-ttu-id="e8700-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8700-154">OUTPUTS</span></span>

### <span data-ttu-id="e8700-155">Microsoft. WindowsAzure. Command. SqlDatabase. Services. Server. IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="e8700-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="e8700-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8700-156">NOTES</span></span>
* <span data-ttu-id="e8700-157">Ha tartomány megadása nélkül hitelesíti magát, és Windows PowerShell 2,0-t használ, a Get-Credential parancsmag a \\ felhasználónévhez tartozó fordított () egységprefixumokat ad eredményül, például \User.</span><span class="sxs-lookup"><span data-stu-id="e8700-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="e8700-158">A Windows PowerShell 3,0 nem adja hozzá a fordított perjelet.</span><span class="sxs-lookup"><span data-stu-id="e8700-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="e8700-159">Ezt a fordított perjelet a **New-AzureSqlDatabaseServerContext** parancsmag *hitelesítő* paramétere nem ismeri fel.</span><span class="sxs-lookup"><span data-stu-id="e8700-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="e8700-160">Az eltávolításhoz az alábbihoz hasonló parancsok használhatók:</span><span class="sxs-lookup"><span data-stu-id="e8700-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="e8700-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8700-161">RELATED LINKS</span></span>

[<span data-ttu-id="e8700-162">Azure SQL-adatbázis-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e8700-162">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="e8700-163">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e8700-163">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="e8700-164">Új – AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e8700-164">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="e8700-165">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e8700-165">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="e8700-166">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e8700-166">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


